---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# GetLogContainerName function


## -description


Retrieves 
   the full path name of the specified container.  This function is 
   used mainly to obtain the full path name of a container referenced in the 
   <a href="https://msdn.microsoft.com/library/windows/hardware/ff541782">CLFS_CONTAINER_INFORMATION</a> structure that is 
   returned in calls to <a href="https://msdn.microsoft.com/a3a374ab-e5e9-47c0-9a62-d880823035b5">ScanLogContainers</a>.
  


## -parameters




### -param hLog [in]


      A handle to the log that is obtained from a successful call to 
      <a href="https://msdn.microsoft.com/ac104bf9-7ca7-417a-bd14-09b0e82c6a77">CreateLogFile</a>. 

The log handle could refer to a 
      log stream or a physical log.
     


### -param cidLogicalContainer [in]


      The unique  identifier that is associated with a container. 


### -param pwstrContainerName [in, out]


      A pointer to a user-allocated buffer to receive the full path and name of the log container, in wide characters.
     


### -param cLenContainerName [in]

The size of the buffer pointed to by <i>pwstrContainerName</i>, in characters.


### -param OPTIONAL

TBD




#### - pcActualLenContainerName [in, out, optional]

A pointer to a variable to receive the actual character count of the full container path name that is retrieved. 
      

If the function succeeds, the value of this parameter is less than or equal to 
      <i>cLenContainerName</i>. If the buffer is not large enough to store the whole container 
      path name, the function fails with <b>ERROR_MORE_DATA</b> and sets this parameter to the 
      size that is required for the full path name. For other failures the value is not defined.
     


## -returns



If the function succeeds, the return value is nonzero. 
      


       If the function fails, the return value is zero (0). To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following list identifies the possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541782">CLFS_CONTAINER_INFORMATION</a>



<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/a3a374ab-e5e9-47c0-9a62-d880823035b5">ScanLogContainers</a>
 

 

