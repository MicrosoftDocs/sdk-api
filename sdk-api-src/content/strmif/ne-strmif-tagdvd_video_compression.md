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

# tagDVD_VIDEO_COMPRESSION enumeration


## -description



Defines the possible DVD video compression types.




## -enum-fields




### -field DVD_VideoCompression_Other


            Unrecognized compression type.
          


### -field DVD_VideoCompression_MPEG1


            MPEG-1 compression type.
          


### -field DVD_VideoCompression_MPEG2


            MPEG-2 compression type.
          


## -remarks



This enumeration is a member of the <a href="https://msdn.microsoft.com/b395a322-d63e-41a0-b97a-88f99aeba0e5">DVD_VideoAttributes</a> structure, which is filled by a call to the <a href="https://msdn.microsoft.com/92bd3af9-7057-4bf7-9026-d4862c271a03">IDvdInfo2::GetCurrentVideoAttributes</a> method.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 

