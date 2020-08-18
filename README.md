# Scala-on-Z

# How to install Scala on LinuxONE Community Cloud
Scala combines object-oriented and functional programming in one concise, high-level language. Scala's static types help avoid bugs in complex applications, and its JVM and JavaScript runtimes let you build high-performance systems with easy access to huge ecosystems of libraries. Great for BigData and ML.
 
In this tutorial, We will be using RHEL (7.8, 8) & SLES 15


## Prerequisites
 1. Request access to LinuxONE Community Cloud. Follow instructions [here](https://github.com/PhilaD1/technical-resources/blob/master/faststart/deploy-virtual-server.md)


### Step 1: Build and Install Scala
 
   1.1 Install the dependencies with OpenJDK and AdoptOpenJDK
   
   For RHEL7.8,8
   ```sh
   # sudo yum install -y java-11-openjdk java-11-openjdk-devel wget
   ```
   <img width="656" alt="Screenshot 2020-08-18 at 10 50 02" src="https://user-images.githubusercontent.com/50323060/90491759-a7f18000-e140-11ea-9476-5edeaea30d44.png">
   
   ```sh
   # sudo yum install -y tar wget
   ```
   <img width="663" alt="Screenshot 2020-08-18 at 10 50 22" src="https://user-images.githubusercontent.com/50323060/90491816-ba6bb980-e140-11ea-8101-aa4f9d1770f9.png">
   
   
   For SLES 15
   ```sh
   # sudo zypper install -y java-11-openjdk java-11-openjdk-devel wget
   ```
   <img width="681" alt="Screenshot 2020-08-18 at 10 45 13" src="https://user-images.githubusercontent.com/50323060/90491370-20a40c80-e140-11ea-9a93-421552bea7e8.png">
   
   <img width="683" alt="Screenshot 2020-08-18 at 10 46 26" src="https://user-images.githubusercontent.com/50323060/90491425-331e4600-e140-11ea-87bf-1429553bbe5c.png">
   
   
   ```sh
   # sudo zypper install -y tar wget gzip
   ```
<img width="685" alt="Screenshot 2020-08-18 at 10 46 05" src="https://user-images.githubusercontent.com/50323060/90491476-45987f80-e140-11ea-87f2-4abee0272b79.png">


### Step 2: Download and Install Scala
   
   2.1 For RHEL and SLES:
   ```sh
   # wget http://www.scala-lang.org/files/archive/scala-2.13.3.rpm
   ```
  
   <img width="650" alt="Screenshot 2020-08-18 at 10 54 11" src="https://user-images.githubusercontent.com/50323060/90492203-382fc500-e141-11ea-8f14-1fd3aa1a8b54.png">

   ```sh
   # sudo rpm -ivh scala-2.13.3.rpm
   ```
   <img width="601" alt="Screenshot 2020-08-18 at 10 57 58" src="https://user-images.githubusercontent.com/50323060/90492792-de7bca80-e141-11ea-8e33-10e1f417765e.png">
   
 
   2.2 Check Scala & Scalac version
   ```sh
   # scala -version
   ```
   
   ```sh 
   Scala code runner version 2.13.3 -- Copyright 2002-2020, LAMP/EPFL and Lightbend, Inc.
   ```
 
   ```sh 
   # scalac -version
    ```
    
   ```sh  
   Scala compiler version 2.13.3 -- Copyright 2002-2020, LAMP/EPFL and Lightbend, Inc.
   ```
  ### Step 3:Testing Scala
  
  3.1 Create at test program
  
   ```sh
   # sudo vi HelloWorld.scala
   ```
   
   ```sh
   # object HelloWorld
{
    def main(args: Array[String]): Unit = {
        println("Hello, world!")
    }
}
   ```
   
   ```sh
   # wq:
   ```

   ```sh
   # scala HelloWorld
   ```
  
  The output of the above should result:
  
   ```sh
   Hello, world!
   ```

   ```sh
   # scala
   ```
   
   ```sh  
   # scala> 16*70
   ```
  
  The output of the above should result:
   ```sh 
   val res0: Int = 1120
   ```

   ```sh 
   # scala> println("Hello Developer")
   ```

 The output of the above should result:
   ```sh 
   Hello Developer
   ```

  ### WELL DONE!
   
   
 
