---
UID: NF:clfsw32.GetLogContainerName
title: GetLogContainerName function (clfsw32.h)
author: windows-sdk-content
description: Retrieves the full path name of the specified container.
old-location: fs\getlogcontainername.htm
tech.root: Clfs
ms.assetid: 4ff12544-797d-48b9-9c42-4bec059e6551
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetLogContainerName, GetLogContainerName function [Files], clfsw32/GetLogContainerName, fs.getlogcontainername
ms.topic: function
req.header: clfsw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - GetLogContainerName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetLogContainerName function


## -description


Retrieves 
   the full path name of the specified container.  This function is 
   used mainly to obtain the full path name of a container referenced in the 
   <a href="https://msdn.microsoft.com/3788fac0-4e99-49e0-bba1-6a6d22299950">CLFS_CONTAINER_INFORMATION</a> structure that is 
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


### -param pcActualLenContainerName [in, out, optional]

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




<a href="https://msdn.microsoft.com/3788fac0-4e99-49e0-bba1-6a6d22299950">CLFS_CONTAINER_INFORMATION</a>



<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/a3a374ab-e5e9-47c0-9a62-d880823035b5">ScanLogContainers</a>
 

 

