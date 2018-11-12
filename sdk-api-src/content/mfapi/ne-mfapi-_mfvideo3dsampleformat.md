---
UID: NE:mfapi._MFVideo3DSampleFormat
title: "_MFVideo3DSampleFormat"
author: windows-sdk-content
description: Specifies how a 3D video frame is stored in a media sample.
old-location: mf\mfvideo3dsampleformat.htm
tech.root: medfound
ms.assetid: 4EC788EC-85C9-41B2-A105-3B6EA040F2B7
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: MFSampleExtension_3DVideo_MultiView, MFSampleExtension_3DVideo_Packed, MFVideo3DSampleFormat, MFVideo3DSampleFormat enumeration [Media Foundation], _MFVideo3DSampleFormat, mf.mfvideo3dsampleformat, mfapi/MFSampleExtension_3DVideo_MultiView, mfapi/MFSampleExtension_3DVideo_Packed, mfapi/MFVideo3DSampleFormat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MFVideo3DSampleFormat
product: Windows
targetos: Windows
req.typenames: MFVideo3DSampleFormat
req.redist: 
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
 

 

