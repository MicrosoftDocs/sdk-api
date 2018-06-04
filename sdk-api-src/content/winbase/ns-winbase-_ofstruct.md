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

# _OFSTRUCT structure


## -description


Contains information about a file that the 
<a href="https://msdn.microsoft.com/800f4d40-252a-44fe-b10d-348c22d69355">OpenFile</a> function opened or attempted to open.


## -struct-fields




### -field cBytes

The size of the structure, in bytes.


### -field fFixedDisk

If this member is nonzero, the file is on a hard (fixed) disk. Otherwise, it is not.


### -field nErrCode

The MS-DOS error code if the 
<a href="https://msdn.microsoft.com/800f4d40-252a-44fe-b10d-348c22d69355">OpenFile</a> function failed.


### -field Reserved1

Reserved; do not use.


### -field Reserved2

Reserved; do not use.


### -field szPathName

The path and file name of the file.


## -see-also




<a href="https://msdn.microsoft.com/800f4d40-252a-44fe-b10d-348c22d69355">OpenFile</a>
 

 

