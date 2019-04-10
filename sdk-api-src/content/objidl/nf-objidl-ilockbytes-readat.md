---
UID: NF:objidl.ILockBytes.ReadAt
title: ILockBytes::ReadAt (objidl.h)
author: windows-sdk-content
description: The ReadAt method reads a specified number of bytes starting at a specified offset from the beginning of the byte array object.
old-location: stg\ilockbytes_readat.htm
tech.root: Stg
ms.assetid: 0478d6f0-65c4-445b-946a-692f2373e8f1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ILockBytes interface [Structured Storage],ReadAt method, ILockBytes.ReadAt, ILockBytes::ReadAt, ReadAt, ReadAt method [Structured Storage], ReadAt method [Structured Storage],ILockBytes interface, _stg_ilockbytes_readat, objidl/ILockBytes::ReadAt, stg.ilockbytes_readat
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - ILockBytes.ReadAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

