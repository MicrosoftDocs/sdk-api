---
UID: NS:wmsdkidl.__tagDRM_PLAY_OPL
title: DRM_PLAY_OPL (wmsdkidl.h)
description: The DRM_PLAY_OPL structure holds information about the output protection levels (OPL) specified in a license for play actions.
helpviewer_keywords: ["DRM_PLAY_OPL","DRM_PLAY_OPL structure [windows Media Format]","structure [windows Media Format]","wmformat.drm_play_opl","wmsdkidl/DRM_PLAY_OPL"]
old-location: wmformat\drm_play_opl.htm
tech.root: wmformat
ms.assetid: 5d14bd02-0fb5-4982-b3dc-7f8277cb852f
ms.date: 4/26/2023
ms.keywords: DRM_PLAY_OPL, DRM_PLAY_OPL structure [windows Media Format], structure [windows Media Format], wmformat.drm_play_opl, wmsdkidl/DRM_PLAY_OPL
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
req.typenames: DRM_PLAY_OPL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __tagDRM_PLAY_OPL
 - wmsdkidl/__tagDRM_PLAY_OPL
 - DRM_PLAY_OPL
 - wmsdkidl/DRM_PLAY_OPL
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
 - DRM_PLAY_OPL
---

# DRM_PLAY_OPL structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>DRM_PLAY_OPL</b> structure holds information about the output protection levels (OPL) specified in a license for play actions.

## -struct-fields

### -field minOPL

<a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels">DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS</a> structure containing the minimum OPL required to play content in different formats.

### -field oplIdReserved

Reserved for future use.

### -field vopi

<a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_video_output_protection_ids">DRM_VIDEO_OUTPUT_PROTECTION_IDS</a> structure containing the video output protection identifiers that apply to playback of the content.

## -see-also

<a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl">DRM_COPY_OPL</a>



<a href="/windows/desktop/wmformat/structures">Structures</a>