---
UID: NE:mfapi._MFVideoDRMFlags
title: MFVideoDRMFlags (mfapi.h)
description: Specifies the type of copy protection required for a video stream.
helpviewer_keywords: ["6d218992-c1c3-4d83-b364-4c7d3b50474f","MFVideoDRMFlag_AnalogProtected","MFVideoDRMFlag_DigitallyProtected","MFVideoDRMFlag_None","MFVideoDRMFlags","MFVideoDRMFlags enumeration [Media Foundation]","mf.mfvideodrmflags","mfapi/MFVideoDRMFlag_AnalogProtected","mfapi/MFVideoDRMFlag_DigitallyProtected","mfapi/MFVideoDRMFlag_None","mfapi/MFVideoDRMFlags"]
old-location: mf\mfvideodrmflags.htm
tech.root: mf
ms.assetid: 6d218992-c1c3-4d83-b364-4c7d3b50474f
ms.date: 12/05/2018
ms.keywords: 6d218992-c1c3-4d83-b364-4c7d3b50474f, MFVideoDRMFlag_AnalogProtected, MFVideoDRMFlag_DigitallyProtected, MFVideoDRMFlag_None, MFVideoDRMFlags, MFVideoDRMFlags enumeration [Media Foundation], mf.mfvideodrmflags, mfapi/MFVideoDRMFlag_AnalogProtected, mfapi/MFVideoDRMFlag_DigitallyProtected, mfapi/MFVideoDRMFlag_None, mfapi/MFVideoDRMFlags
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: MFVideoDRMFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFVideoDRMFlags
 - mfapi/_MFVideoDRMFlags
 - MFVideoDRMFlags
 - mfapi/MFVideoDRMFlags
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
 - MFVideoDRMFlags
---

# MFVideoDRMFlags enumeration


## -description

Specifies the type of copy protection required for a video stream.

## -enum-fields

### -field MFVideoDRMFlag_None:0

No copy protection is required.

### -field MFVideoDRMFlag_AnalogProtected:1

Analog copy protection should be applied.

### -field MFVideoDRMFlag_DigitallyProtected:2

Digital copy protection should be applied.

## -remarks

Use these flags with the <a href="/windows/desktop/medfound/mf-mt-drm-flags-attribute">MF_MT_DRM_FLAGS</a> attribute.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
