---
UID: NF:clfsw32.AddLogContainerSet
title: AddLogContainerSet function
author: windows-sdk-content
description: Adds multiple log containers to the physical log that is associated with the log handle&#8212;if the calling process has access to the log handle.
old-location: fs\addlogcontainerset.htm
tech.root: Clfs
ms.assetid: b3dec3bd-3e39-42fa-8f73-71784b3d5be2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AddLogContainerSet, AddLogContainerSet function [Files], clfsw32/AddLogContainerSet, fs.addlogcontainerset
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - AddLogContainerSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AddLogContainerSet function


## -description


Adds multiple log containers to the physical log  that is associated with the log handle—if the calling process has access to the log handle.  Adding containers allows a client to increase the size of a log.


## -parameters




### -param hLog [in]

The handle to an open log that is obtained from <a href="https://msdn.microsoft.com/ac104bf9-7ca7-417a-bd14-09b0e82c6a77">CreateLogFile</a> with permissions to add a log container. 

The file can be dedicated or multiplexed.


### -param cContainer [in]

The number of containers  in the <i>rgwszContainerPath</i> array.  

This value must be nonzero.  A log must have at least two containers before any I/O can be performed on it.


### -param pcbContainer [in, optional]

The size of the container, in bytes.  

The minimum size is  512 KB for normal logs and 1024 KB for multiplexed logs. The maximum size is approximately 4 gigabytes (GB).

This parameter is required if the containers are being added to a newly created log.  If a container is already created, this parameter can  be <b>NULL</b>, or some value that is at least as large as the size of the first container. 


Log container sizes are multiples of the log region size  (512 KB).  When you add a container to a new file, the <a href="https://msdn.microsoft.com/5e886b96-9431-43f6-b888-e0f47c432371">AddLogContainer</a> function rounds the size of the container up to the next 512 KB boundary, and returns that size in the value pointed to by <i>pcbContainer</i>.  

Similarly,  if the log already has at least one container and the value of <i>*pcbContainer</i> is at least as large as the current container size, the function creates all containers with the current internal size and returns that size in <i>*pcbContainer</i>.


### -param rgwszContainerPath [in]

An array of   <i>cContainer</i> path names for containers.  

Each element in the array is a wide-character string that contains a valid path for the new container in the log volume.


### -param pReserved [in, out, optional]

Reserved.  Set <i>Reserved</i> to <b>NULL</b>.


## -returns



If the function succeeds, the return value is nonzero, which indicates that all containers are added successfully to the log.

If the function fails, the return value is zero, which indicates that none of the containers are added.  To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following list identifies the possible error codes:




## -remarks



		The <b>AddLogContainerSet</b> function is not atomic.  If the operation 
		is interrupted, for example, by an invalid path name, the call to 
		<b>AddLogContainerSet</b> returns a failure, but some containers may 
		have been created.  Your application must recover from this error, for example, by determining which containers were added.

Because <b>AddLogContainerSet</b> adds more than one container, it is  more
          efficient than making repeated calls to <a href="https://msdn.microsoft.com/5e886b96-9431-43f6-b888-e0f47c432371">AddLogContainer</a>, which only adds one container.

Containers are created and opened in a noncompressed mode, and are initialized with 0 (zeros) when they are created.




## -see-also




<a href="https://msdn.microsoft.com/5e886b96-9431-43f6-b888-e0f47c432371">AddLogContainer</a>



<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>
 

 

