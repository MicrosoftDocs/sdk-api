---
UID: NE:mfapi._MFVideo3DSampleFormat
title: MFVideo3DSampleFormat (mfapi.h)
description: Specifies how a 3D video frame is stored in a media sample.
helpviewer_keywords: ["MFSampleExtension_3DVideo_MultiView","MFSampleExtension_3DVideo_Packed","MFVideo3DSampleFormat","MFVideo3DSampleFormat enumeration [Media Foundation]","mf.mfvideo3dsampleformat","mfapi/MFSampleExtension_3DVideo_MultiView","mfapi/MFSampleExtension_3DVideo_Packed","mfapi/MFVideo3DSampleFormat"]
old-location: mf\mfvideo3dsampleformat.htm
tech.root: mf
ms.assetid: 4EC788EC-85C9-41B2-A105-3B6EA040F2B7
ms.date: 12/05/2018
ms.keywords: MFSampleExtension_3DVideo_MultiView, MFSampleExtension_3DVideo_Packed, MFVideo3DSampleFormat, MFVideo3DSampleFormat enumeration [Media Foundation], mf.mfvideo3dsampleformat, mfapi/MFSampleExtension_3DVideo_MultiView, mfapi/MFSampleExtension_3DVideo_Packed, mfapi/MFVideo3DSampleFormat
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
targetos: Windows
req.typenames: MFVideo3DSampleFormat
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFVideo3DSampleFormat
 - mfapi/_MFVideo3DSampleFormat
 - MFVideo3DSampleFormat
 - mfapi/MFVideo3DSampleFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - MFVideo3DSampleFormat
---

# MFVideo3DSampleFormat enumeration


## -description

Specifies how a 3D video frame is stored in a media sample.

## -enum-fields

### -field MFSampleExtension_3DVideo_MultiView:1

Each view is stored in a separate buffer. The sample contains one buffer per view.

### -field MFSampleExtension_3DVideo_Packed:0

All of the views are stored in the same buffer. The sample contains a single buffer.

## -remarks

This enumeration is used with the <a href="/windows/desktop/medfound/mfsampleextension-3dvideo-sampleformat">MFSampleExtension_3DVideo_SampleFormat</a> attribute.

The exact layout of the views in memory is specified by the following media type attributes:<ul>
<li>
<a href="/windows/desktop/medfound/mf-mt-video-3d-format">MF_MT_VIDEO_3D_FORMAT</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-mt-video-3d-first-is-left">MF_MT_VIDEO_3D_FIRST_IS_LEFT</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-mt-video-3d-left-is-base">MF_MT_VIDEO_3D_LEFT_IS_BASE</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-mt-video-3d-num-views">MF_MT_VIDEO_3D_NUM_VIEWS</a>
</li>
</ul>

## -see-also

Media Foundation Enumerations
