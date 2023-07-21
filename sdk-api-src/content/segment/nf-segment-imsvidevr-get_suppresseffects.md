---
UID: NF:segment.IMSVidEVR.get_SuppressEffects
title: IMSVidEVR::get_SuppressEffects (segment.h)
description: The get_SuppressEffects method queries whether the Video Control configures the system for optimal video playback
helpviewer_keywords: ["IMSVidEVR interface [Microsoft TV Technologies]","get_SuppressEffects method","IMSVidEVR.get_SuppressEffects","IMSVidEVR::get_SuppressEffects","IMSVidEVRget_SuppressEffects","get_SuppressEffects","get_SuppressEffects method [Microsoft TV Technologies]","get_SuppressEffects method [Microsoft TV Technologies]","IMSVidEVR interface","mstv.imsvidevr_get_suppresseffects","segment/IMSVidEVR::get_SuppressEffects"]
old-location: mstv\imsvidevr_get_suppresseffects.htm
tech.root: mstv
ms.assetid: a3aaf310-6c42-4013-a3bf-25f9c42cdf81
ms.date: 12/05/2018
ms.keywords: IMSVidEVR interface [Microsoft TV Technologies],get_SuppressEffects method, IMSVidEVR.get_SuppressEffects, IMSVidEVR::get_SuppressEffects, IMSVidEVRget_SuppressEffects, get_SuppressEffects, get_SuppressEffects method [Microsoft TV Technologies], get_SuppressEffects method [Microsoft TV Technologies],IMSVidEVR interface, mstv.imsvidevr_get_suppresseffects, segment/IMSVidEVR::get_SuppressEffects
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidEVR::get_SuppressEffects
 - segment/IMSVidEVR::get_SuppressEffects
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidEVR.get_SuppressEffects
---

# IMSVidEVR::get_SuppressEffects


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_SuppressEffects</b> method queries whether the <a href="/previous-versions/windows/desktop/legacy/ee663618(v=vs.85)">Video Control</a> configures the system for optimal video playback

## -parameters

### -param bSuppress [out]

Receives a <b>VARIANT_BOOL</b>. For more information, see <a href="/windows/desktop/api/segment/nf-segment-imsvidevr-put_suppresseffects">IMSVidEVR::put_SuppressEffects</a>. The default value is VARIANT_TRUE.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidevr">IMSVidEVR</a>