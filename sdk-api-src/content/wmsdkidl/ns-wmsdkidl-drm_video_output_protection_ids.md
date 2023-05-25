---
UID: NS:wmsdkidl.__tagDRM_VIDEO_OUTPUT_PROTECTION_IDS
title: DRM_VIDEO_OUTPUT_PROTECTION_IDS (wmsdkidl.h)
description: The DRM_VIDEO_OUTPUT_PROTECTION_IDS structure holds an array of DRM_VIDEO_OUTPUT_PROTECTION structures.
helpviewer_keywords: ["DRM_VIDEO_OUTPUT_PROTECTION_IDS","DRM_VIDEO_OUTPUT_PROTECTION_IDS structure [windows Media Format]","structure [windows Media Format]","wmformat.drm_video_output_protection_ids","wmsdkidl/DRM_VIDEO_OUTPUT_PROTECTION_IDS"]
old-location: wmformat\drm_video_output_protection_ids.htm
tech.root: wmformat
ms.assetid: 95bce5f8-5230-4b69-b4e9-3cb766edce90
ms.date: 4/26/2023
ms.keywords: DRM_VIDEO_OUTPUT_PROTECTION_IDS, DRM_VIDEO_OUTPUT_PROTECTION_IDS structure [windows Media Format], structure [windows Media Format], wmformat.drm_video_output_protection_ids, wmsdkidl/DRM_VIDEO_OUTPUT_PROTECTION_IDS
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
req.typenames: DRM_VIDEO_OUTPUT_PROTECTION_IDS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __tagDRM_VIDEO_OUTPUT_PROTECTION_IDS
 - wmsdkidl/__tagDRM_VIDEO_OUTPUT_PROTECTION_IDS
 - DRM_VIDEO_OUTPUT_PROTECTION_IDS
 - wmsdkidl/DRM_VIDEO_OUTPUT_PROTECTION_IDS
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
 - DRM_VIDEO_OUTPUT_PROTECTION_IDS
---

# DRM_VIDEO_OUTPUT_PROTECTION_IDS structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>DRM_VIDEO_OUTPUT_PROTECTION_IDS</b> structure holds an array of <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_output_protection">DRM_VIDEO_OUTPUT_PROTECTION</a> structures.

## -struct-fields

### -field cEntries

Number of elements in the array referenced by <b>rgVop</b>.

### -field rgVop

Address of an array of <b>DRM_VIDEO_OUTPUT_PROTECTION</b> structures.

## -remarks

This structure is used as a member of the <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl">DRM_PLAY_OPL</a> structure.

## -see-also

<a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_output_protection">DRM_VIDEO_OUTPUT_PROTECTION</a>



<a href="/windows/desktop/wmformat/structures">Structures</a>