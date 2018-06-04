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

# _PLEX_READ_DATA_REQUEST structure


## -description


Indicates the range of the read operation to perform and the plex from which to read.


## -struct-fields




### -field ByteOffset

The offset of the range to be read. The offset can be the virtual offset to a file or volume. File offsets should be cluster aligned and volume offsets should be sector aligned.
					


### -field ByteLength

The length of the range to be read. The maximum value is 64 KB. 


### -field PlexNumber

The plex from which to read. A value of zero indicates the primary copy, a value of one indicates the secondary copy, and so on.


## -see-also




<a href="https://msdn.microsoft.com/f2cddd4d-cb58-484c-9a85-274b88ec4ece">FSCTL_READ_FROM_PLEX</a>
 

 

