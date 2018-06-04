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

# _MFVideo3DSampleFormat enumeration


## -description


Specifies how a 3D video frame is stored in a media sample.


## -enum-fields




### -field MFSampleExtension_3DVideo_MultiView

Each view is stored in a separate buffer. The sample contains one buffer per view.


### -field MFSampleExtension_3DVideo_Packed

All of the views are stored in the same buffer. The sample contains a single buffer. 


## -remarks



This enumeration is used with the <a href="https://msdn.microsoft.com/1B996B22-C76B-47E5-8937-1E5E672E32EC">MFSampleExtension_3DVideo_SampleFormat</a> attribute.

The exact layout of the views in memory is specified by the following media type attributes:<ul>
<li>
<a href="https://msdn.microsoft.com/880DF017-5841-4C0A-82AF-F092DEF5406B">MF_MT_VIDEO_3D_FORMAT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4F33BF2D-EB32-46B6-B071-F9130D404201">MF_MT_VIDEO_3D_FIRST_IS_LEFT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/11555BA0-D9BE-4239-A857-C9EEE86A8520">MF_MT_VIDEO_3D_LEFT_IS_BASE</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5D8224E3-94B1-4056-8424-9978D2B88B3A">MF_MT_VIDEO_3D_NUM_VIEWS</a>
</li>
</ul>





## -see-also




Media Foundation Enumerations
 

 

