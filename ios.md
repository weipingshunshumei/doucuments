
## 模拟器
- 模拟器的文件在mac上的路径：[xcode6.0+] /Users/pingshunwei/Library/Developer/CoreSimulator/Devices 路径下每个文件夹名称就是模拟器的UUID
- 模拟器UUID查看方法：hardware => devices => manager devices 
- 模拟器上的应用目录：
  /Users/pingshunwei/Library/Developer/CoreSimulator/Devices/2C96C681-3471-4771-B2BD-5F703B796E9F/data/Containers/Data/Application  路径下每个文件夹名称是应用的UUID


## ios写文件
- documents目录：
  - 获取应用的documents方法：

	```objc
		+(NSString*) getDocumentDir {
		    NSArray * paths = NSSearchPathForDirectoriesInDomains(NSDocumentDirectory,
		                                                          NSUserDomainMask,
		                                                          YES);
		    if ([paths count] > 0) {
		        return [paths objectAtIndex:0];
		    }
		    return nil;
		}
	```

  - 向documents目录写文件方法：

	`

	    NSString *bodyFileName = [@"body." stringByAppendingString:uploadTimeStr];
	    NSString *fileName = [[SmUtils getDocumentDir
	                 stringByAppendingPathComponent:bodyFileName];
		[writeData writeToFile:fileName atomically:FALSE];
	`

## 字符串
- 字符串拼接:
`

  NSString *bodyFileName = [@"body." stringByAppendingString:uploadTimeStr];
`

## NSArray
- 数组长度   [NSArry count];
