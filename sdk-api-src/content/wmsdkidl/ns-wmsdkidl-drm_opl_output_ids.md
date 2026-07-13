---
UID: NS:wmsdkidl.__tagDRM_OPL_OUTPUT_IDS
title: DRM_OPL_OUTPUT_IDS (wmsdkidl.h)
description: The DRM_OPL_OUTPUT_IDS structure holds a number of output protection level (OPL) output identifiers.
helpviewer_keywords: ["DRM_OPL_OUTPUT_IDS","DRM_OPL_OUTPUT_IDS structure [windows Media Format]","structure [windows Media Format]","wmformat.drm_opl_output_ids","wmsdkidl/DRM_OPL_OUTPUT_IDS"]
old-location: wmformat\drm_opl_output_ids.htm
tech.root: wmformat
ms.assetid: a1f0e1ad-0ba4-4c42-aff5-c5fb4133e0fa
ms.date: 4/26/2023
ms.keywords: DRM_OPL_OUTPUT_IDS, DRM_OPL_OUTPUT_IDS structure [windows Media Format], structure [windows Media Format], wmformat.drm_opl_output_ids, wmsdkidl/DRM_OPL_OUTPUT_IDS
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
req.typenames: DRM_OPL_OUTPUT_IDS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __tagDRM_OPL_OUTPUT_IDS
 - wmsdkidl/__tagDRM_OPL_OUTPUT_IDS
 - DRM_OPL_OUTPUT_IDS
 - wmsdkidl/DRM_OPL_OUTPUT_IDS
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
 - DRM_OPL_OUTPUT_IDS
---

# DRM_OPL_OUTPUT_IDS structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>DRM_OPL_OUTPUT_IDS</b> structure holds a number of output protection level (OPL) output identifiers.

## -struct-fields

### -field cIds

Number of identifiers in the array referenced by <b>rgIds</b>.

### -field rgIds

Address of an array of GUIDs. Each member of the array contains an OPL output identifier.

## -remarks

This structure is used as a member of the <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl">DRM_COPY_OPL</a> and <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl">DRM_PLAY_OPL</a> structures to identify groups of output identifiers.

## -see-also

<a href="/windows/desktop/wmformat/structures">Structures</a>