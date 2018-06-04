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

# _FILE_STREAM_INFO structure


## -description


Receives  file stream information for the specified file. Used for any handles. Use only when calling <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>.


## -struct-fields




### -field NextEntryOffset

The offset for the next <b>FILE_STREAM_INFO</b> entry that is returned. This member is zero if no other entries follow this one. 



### -field StreamNameLength

The length, in bytes, of <b>StreamName</b>.


### -field StreamSize

The size, in bytes,  of the data stream.


### -field StreamAllocationSize

The amount of space that  is allocated for the stream, in bytes.  This value is usually a multiple of the sector or cluster size of the underlying physical device.


### -field StreamName

The stream name.


## -remarks



The <b>FILE_STREAM_INFO</b> structure is used to enumerate the streams for a file.



Support for named data streams is file-system-specific. 



The <b>FILE_STREAM_INFO</b> structure must be aligned on a <b>LONGLONG</b> (8-byte) boundary. If a buffer contains two or more of these structures, the <b>NextEntryOffset</b> value in each entry, except the last, falls on an 8-byte boundary.




## -see-also




<a href="https://msdn.microsoft.com/8f02e824-ca41-48c1-a5e8-5b12d81886b5">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>
 

 

