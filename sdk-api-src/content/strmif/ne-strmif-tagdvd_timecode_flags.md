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

# tagDVD_TIMECODE_FLAGS enumeration


## -description



Indicates the frame rate at which a DVD has been authored to play.




## -enum-fields




### -field DVD_TC_FLAG_25fps

Disc is authored to play at 25 frames per second.


### -field DVD_TC_FLAG_30fps

Disc is authored to play at 30 frames per second.


### -field DVD_TC_FLAG_DropFrame

Disc is authored to play at 29.97 frames per second.


### -field DVD_TC_FLAG_Interpolated

Value representing the <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator Filter</a> filter's best estimate of the disc's frame rate.


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/90768da1-592a-49ec-99b0-56f463c322e8">IDvdInfo2::GetTotalTitleTime</a>
 

 

