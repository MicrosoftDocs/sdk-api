---
UID: NS:wmsdkidl._WMT_COLORSPACEINFO_EXTENSION_DATA
title: WMT_COLORSPACEINFO_EXTENSION_DATA (wmsdkidl.h)
description: The WMT_COLORSPACEINFO_EXTENSION_DATA structure contains information about the color format of output video samples. It is used as the value for the WM_SampleExtensionGUID_ColorSpaceInfo data unit extension.
helpviewer_keywords: ["WMT_COLORSPACEINFO_EXTENSION_DATA","WMT_COLORSPACEINFO_EXTENSION_DATA structure [windows Media Format]","wmformat.wmt_colorspaceinfo_extension_data","wmsdkidl/WMT_COLORSPACEINFO_EXTENSION_DATA"]
old-location: wmformat\wmt_colorspaceinfo_extension_data.htm
tech.root: wmformat
ms.assetid: 0d512d6a-95d5-4ca1-aee2-ca19319e1b83
ms.date: 4/26/2023
ms.keywords: WMT_COLORSPACEINFO_EXTENSION_DATA, WMT_COLORSPACEINFO_EXTENSION_DATA structure [windows Media Format], wmformat.wmt_colorspaceinfo_extension_data, wmsdkidl/WMT_COLORSPACEINFO_EXTENSION_DATA
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
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
req.typenames: WMT_COLORSPACEINFO_EXTENSION_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WMT_COLORSPACEINFO_EXTENSION_DATA
 - wmsdkidl/_WMT_COLORSPACEINFO_EXTENSION_DATA
 - WMT_COLORSPACEINFO_EXTENSION_DATA
 - wmsdkidl/WMT_COLORSPACEINFO_EXTENSION_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WMT_COLORSPACEINFO_EXTENSION_DATA
---

# WMT_COLORSPACEINFO_EXTENSION_DATA structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WMT_COLORSPACEINFO_EXTENSION_DATA</b> structure contains information about the color format of output video samples. It is used as the value for the WM_SampleExtensionGUID_ColorSpaceInfo data unit extension.

## -struct-fields

### -field ucColorPrimaries

Specifies the chromaticity coordinates of the color primaries.

### -field ucColorTransferChar

Specifies the opto-electronic transfer characteristics of the source picture.

### -field ucColorMatrixCoef

Specifies the matrix coefficients used to derive Y, Cb, and Cr signals from the color primaries.

## -see-also

<a href="/windows/desktop/wmformat/sample-extension-types">Sample Extension Types</a>



<a href="/windows/desktop/wmformat/structures">Structures</a>