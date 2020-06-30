# Detection-Using-Convolutional-Networks
 OverFeat: Integrated Recognition, Localization and Detection Using Convolutional Networks. arXiv:1312.6229 [Cs], December, 2013.


#### Apple 의 An On-device Deep Neural Network for Face Detection 에 사용 및 참고된 논문을 구현하는 프로젝트입니다.
- Vol. 1, Issue 7 ∙ November 2017 
- by Computer Vision Machine Learning Team


#### Issues List

- Issue 1 => Model Parameters Issue, [https://github.com/LeeGitaek/Detection-Using-Convolutional-Networks/issues/1]

### Model Structure

- Layer 1
   => Conv + Max Pooling, 
      Channel => 96, 
      Filter size (Kernel) => 11 * 11, 
      Conv Stride => 4 * 4, 
      Pooling Size => 2 * 2, 
      Pooling Stride => 2 * 2,
      Zero Padding Size => -,
      Spartial Input Size => 231 * 231
      
      
- Layer 2
   => Conv + Max Pooling, 
      Channel => 256, 
      Filter size (Kernel) => 5 * 5, 
      Conv Stride => 1 * 1, 
      Pooling Size => 2 * 2, 
      Pooling Stride => 2 * 2,
      Zero Padding Size => -,
      Spartial Input Size => 24 * 24
      
      
- Layer 3
   => Conv,
      Channel => 512, 
      Filter size (Kernel) => 3 * 3, 
      Conv Stride => 1 * 1, 
      Pooling Size => -, 
      Pooling Stride => -,
      Zero Padding Size => 1 * 1 * 1 * 1,
      Spartial Input Size => 12 * 12
      
- Layer 4
   => Conv,
      Channel => 1024, 
      Filter size (Kernel) => 3 * 3, 
      Conv Stride => 1 * 1, 
      Pooling Size => -, 
      Pooling Stride => -,
      Zero Padding Size => 1 * 1 * 1 * 1,
      Spartial Input Size => 12 * 12
      
- Layer 5
   => Conv + Max Pooling,
      Channel => 1024, 
      Filter size (Kernel) => 3 * 3, 
      Conv Stride => 1 * 1, 
      Pooling Size => 2 * 2, 
      Pooling Stride => 2 * 2,
      Zero Padding Size => 1 * 1 * 1 * 1,
      Spartial Input Size => 12 * 12
     
#### FC ( Fully Connected Layer )
- Layer 6
   => Full ,
      Channel => 3072, 
      Filter size (Kernel) => -, 
      Conv Stride => -, 
      Pooling Size => -, 
      Pooling Stride => -,
      Zero Padding Size => -,
      Spartial Input Size => 6 * 6
   
- Layer 7
   => Full ,
      Channel => 4096, 
      Filter size (Kernel) => -, 
      Conv Stride => -, 
      Pooling Size => -, 
      Pooling Stride => -,
      Zero Padding Size => -,
      Spartial Input Size => 1 * 1
      
#### Output Layer 
- Layer 8
   => Full ,
      Channel => 1000, 
      Filter size (Kernel) => -, 
      Conv Stride => -, 
      Pooling Size => -, 
      Pooling Stride => -,
      Zero Padding Size => -,
      Spartial Input Size => 1 * 1
