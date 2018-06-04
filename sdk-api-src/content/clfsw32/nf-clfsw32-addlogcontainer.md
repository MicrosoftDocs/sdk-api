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

# AddLogContainer function


## -description


Adds a container to the physical log  that is associated with the log handle—if the calling process has  write access to the .blf file and the ability to create files in the target directory of the container.

This function is different from  <a href="https://msdn.microsoft.com/b3dec3bd-3e39-42fa-8f73-71784b3d5be2">AddLogContainerSet</a>, because it  adds only one  container.  To add multiple containers,  it is  more efficient to use <b>AddLogContainerSet</b>, which allows you to add more than one container. Adding containers allows a client to increase the size of a log.


## -parameters




### -param hLog [in]

The handle to an open log. 

The handle must  be   obtained from <a href="https://msdn.microsoft.com/ac104bf9-7ca7-417a-bd14-09b0e82c6a77">CreateLogFile</a> with write access to the log. The client application must have  write access to the .blf file, and the ability to create files in the target directory of a container.


### -param pcbContainer [in, optional]

The optional parameter that specifies the size of the container, in bytes.  

The minimum size is  512 KB for normal logs and 1024 KB for multiplexed logs. The maximum size is approximately 4 gigabytes.

This parameter is required if the containers are being added to a newly created log.  If a container is already created, this parameter can  be <b>NULL</b>, or some value that is at least as large as the size of the first container. 


Log container sizes are multiples of the log region size  (512 KB).  When you add a container to a new file, the <b>AddLogContainer</b> function rounds the size of the container up to the next 512 KB boundary, and returns that size in the value pointed to by <i>pcbContainer</i>.  

Similarly,  if the log already has at least one container and the value of <i>*pcbContainer</i> is at least as large as the current container size, the function creates all containers with the current internal size and returns that size in <i>*pcbContainer</i>.


### -param pwszContainerPath [in]

A pointer to a null-terminated string that contains a valid path for the new container on a log volume.


### -param pReserved [in, out, optional]

Reserved.  Set <i>pReserved</i> to <b>NULL</b>.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following list identifies the possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/b3dec3bd-3e39-42fa-8f73-71784b3d5be2">AddLogContainerSet</a>



<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/ac104bf9-7ca7-417a-bd14-09b0e82c6a77">CreateLogFile</a>
 

 

