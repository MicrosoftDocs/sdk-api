---
UID: NS:wmsdkidl.__tagDRM_OUTPUT_PROTECTION
title: DRM_OUTPUT_PROTECTION (wmsdkidl.h)
description: The DRM_VIDEO_OUTPUT_PROTECTION structure holds a video output technology identifier and the configuration data required by that technology.
helpviewer_keywords: ["DRM_OUTPUT_PROTECTION","DRM_VIDEO_OUTPUT_PROTECTION","DRM_VIDEO_OUTPUT_PROTECTION structure [windows Media Format]","structure [windows Media Format]","wmformat.drm_video_output_protection","wmsdkidl/DRM_VIDEO_OUTPUT_PROTECTION"]
old-location: wmformat\drm_video_output_protection.htm
tech.root: wmformat
ms.assetid: 73c7b2ab-3680-462a-ab7f-d3270ea0127b
ms.date: 12/05/2018
ms.keywords: DRM_OUTPUT_PROTECTION, DRM_VIDEO_OUTPUT_PROTECTION, DRM_VIDEO_OUTPUT_PROTECTION structure [windows Media Format], structure [windows Media Format], wmformat.drm_video_output_protection, wmsdkidl/DRM_VIDEO_OUTPUT_PROTECTION
req.header: wmsdkidl.h
req.include-header: Drmexternals.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: DRM_OUTPUT_PROTECTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __tagDRM_OUTPUT_PROTECTION
 - wmsdkidl/__tagDRM_OUTPUT_PROTECTION
 - DRM_OUTPUT_PROTECTION
 - wmsdkidl/DRM_OUTPUT_PROTECTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmsdkidl.h
api_name:
 - DRM_VIDEO_OUTPUT_PROTECTION
---

# DRM_OUTPUT_PROTECTION structure


## -description

The <b>DRM_VIDEO_OUTPUT_PROTECTION</b> structure holds a video output technology identifier and the configuration data required by that technology.

## -struct-fields

### -field guidId

Technology identifier.

### -field bConfigData

Configuration data required by the technology identified by <b>guidId</b>.

## -remarks

The <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_video_output_protection_ids">DRM_VIDEO_OUTPUT_PROTECTION_IDS</a> structure contains an array of <b>DRM_VIDEO_OUTPUT_PROTECTION</b> structures.

## -see-also

<a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_video_output_protection_ids">DRM_VIDEO_OUTPUT_PROTECTION_IDS</a>



<a href="/windows/desktop/wmformat/structures">Structures</a>