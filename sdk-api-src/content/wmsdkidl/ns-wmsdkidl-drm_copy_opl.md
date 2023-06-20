---
UID: NS:wmsdkidl.__tagDRM_COPY_OPL
title: DRM_COPY_OPL (wmsdkidl.h)
description: The DRM_COPY_OPL structure holds information about the output protection levels specified in a license for copy actions.
helpviewer_keywords: ["DRM_COPY_OPL","DRM_COPY_OPL structure [windows Media Format]","structure [windows Media Format]","wmformat.drm_copy_opl","wmsdkidl/DRM_COPY_OPL"]
old-location: wmformat\drm_copy_opl.htm
tech.root: wmformat
ms.assetid: cf35626a-5583-440f-8f17-0c9b79bd843d
ms.date: 4/26/2023
ms.keywords: DRM_COPY_OPL, DRM_COPY_OPL structure [windows Media Format], structure [windows Media Format], wmformat.drm_copy_opl, wmsdkidl/DRM_COPY_OPL
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
req.typenames: DRM_COPY_OPL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __tagDRM_COPY_OPL
 - wmsdkidl/__tagDRM_COPY_OPL
 - DRM_COPY_OPL
 - wmsdkidl/DRM_COPY_OPL
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
 - DRM_COPY_OPL
---

# DRM_COPY_OPL structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>DRM_COPY_OPL</b> structure holds information about the output protection levels specified in a license for copy actions.

## -struct-fields

### -field wMinimumCopyLevel

Minimum output protection level for copy actions.

### -field oplIdIncludes

<a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_opl_output_ids">DRM_OPL_OUTPUT_IDS</a> structure containing the identifiers of technologies to allow. This member is used for output technologies that are assigned OPLs lower than the minimum copy level, but to which the content may be copied.

### -field oplIdExcludes

<a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_opl_output_ids">DRM_OPL_OUTPUT_IDS</a> structure containing the output identifiers of technologies to restrict. This member is used for output technologies that are assigned OPLs that exceed the minimum copy level, but that the license issuer does not grant rights for copying to.

## -see-also

<a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl">DRM_PLAY_OPL</a>



<a href="/windows/desktop/wmformat/structures">Structures</a>