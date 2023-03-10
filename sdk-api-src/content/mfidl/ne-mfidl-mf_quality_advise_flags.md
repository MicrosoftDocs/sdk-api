---
UID: NE:mfidl._MF_QUALITY_ADVISE_FLAGS
title: MF_QUALITY_ADVISE_FLAGS (mfidl.h)
description: Contains flags for the IMFQualityAdvise2::NotifyQualityEvent method.
helpviewer_keywords: ["MF_QUALITY_ADVISE_FLAGS","MF_QUALITY_ADVISE_FLAGS enumeration [Media Foundation]","MF_QUALITY_CANNOT_KEEP_UP","mf.mf_quality_advise_flags","mfidl/MF_QUALITY_ADVISE_FLAGS","mfidl/MF_QUALITY_CANNOT_KEEP_UP"]
old-location: mf\mf_quality_advise_flags.htm
tech.root: mf
ms.assetid: 93cf5585-fcb4-480a-b482-241376e8ec73
ms.date: 12/05/2018
ms.keywords: MF_QUALITY_ADVISE_FLAGS, MF_QUALITY_ADVISE_FLAGS enumeration [Media Foundation], MF_QUALITY_CANNOT_KEEP_UP, mf.mf_quality_advise_flags, mfidl/MF_QUALITY_ADVISE_FLAGS, mfidl/MF_QUALITY_CANNOT_KEEP_UP
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: MF_QUALITY_ADVISE_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MF_QUALITY_ADVISE_FLAGS
 - mfidl/_MF_QUALITY_ADVISE_FLAGS
 - MF_QUALITY_ADVISE_FLAGS
 - mfidl/MF_QUALITY_ADVISE_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MF_QUALITY_ADVISE_FLAGS
---

# MF_QUALITY_ADVISE_FLAGS enumeration


## -description

Contains flags for the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise2-notifyqualityevent">IMFQualityAdvise2::NotifyQualityEvent</a> method.

## -enum-fields

### -field MF_QUALITY_CANNOT_KEEP_UP:0x1

The decoder has done everything that it can to reduce sample latency, and samples are still late.

## -remarks

If the decoder sets the <b>MF_QUALITY_CANNOT_KEEP_UP</b> flag, the quality manager tries to reduce latency through the media source and the media sink. For example, it might request the <a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a> (EVR) to drop frames. During this period, the quality manager stops calling the decoder's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise2-notifyqualityevent">IMFQualityAdvise2::NotifyQualityEvent</a> method, until samples are no longer arriving late at the sink. At that point, the quality manager resumes calling <b>NotifyQualityEvent</b> on the decoder.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2">IMFQualityAdvise2</a>



<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
