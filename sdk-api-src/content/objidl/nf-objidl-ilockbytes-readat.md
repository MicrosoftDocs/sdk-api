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

# ILockBytes::ReadAt


## -description


The <b>ReadAt</b> method reads a specified number of bytes starting at a specified offset from the beginning of the byte array object.


## -parameters




### -param ulOffset [in]

Specifies the starting point from the beginning of the byte array for reading data.


### -param pv [in]

Pointer to the buffer into which the byte array is read.  The size of this buffer is contained in <i>cb</i>.


### -param cb [in]

Specifies the number of bytes of data to attempt to read from the byte array.


### -param pcbRead [out]

Pointer to a <b>ULONG</b> where this method writes the actual number of bytes read from the byte array. You can set this pointer to <b>NULL</b> to indicate that you are not interested in this value. In this case, this method does not provide the actual number of bytes that were read.


## -returns



This method can return one of these values.




## -remarks



<b>ILockBytes::ReadAt</b> reads bytes from the byte array object. It reports the number of bytes that were actually read. This value may be less than the number of bytes requested if an error occurs or if the end of the byte array is reached during the read.

It is not an error to read less than the specified number of bytes if the operation encounters the end of the byte array. Note that this is the same end-of-file behavior as found in MS-DOS file allocation table (FAT) file system files.




## -see-also




<a href="https://msdn.microsoft.com/700b6a3c-1046-4c21-8887-16f344c23510">ILockBytes - File-Based Implementation</a>



<a href="https://msdn.microsoft.com/6ab019b0-34d7-4b6e-ba77-6b6881fabd29">ILockBytes - Global Memory Implementation</a>



<a href="https://msdn.microsoft.com/a27af4e1-293d-438a-8068-87275a51fd48">ILockBytes::WriteAt</a>
 

 

