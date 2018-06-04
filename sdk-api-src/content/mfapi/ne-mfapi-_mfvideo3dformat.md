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

# _MFVideo3DFormat enumeration


## -description


Specifies how 3D video frames are stored in memory.


## -enum-fields




### -field MFVideo3DSampleFormat_BaseView

The base view is stored in a single buffer. The other view is discarded.


### -field MFVideo3DSampleFormat_MultiView

Each media sample contains multiple buffers, one for each view.


### -field MFVideo3DSampleFormat_Packed_LeftRight

Each media sample contains one buffer, with both views packed side-by-side into a single frame. 


### -field MFVideo3DSampleFormat_Packed_TopBottom

Each media sample contains one buffer, with both views packed top-and-bottom into a single frame. 


## -remarks



This enumeration is used with the <a href="https://msdn.microsoft.com/880DF017-5841-4C0A-82AF-F092DEF5406B">MF_MT_VIDEO_3D_FORMAT</a> attribute.




## -see-also




Media Foundation Enumerations
 

 

