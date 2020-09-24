---
UID: NS:wmsdkidl._WMT_WEBSTREAM_FORMAT
title: WMT_WEBSTREAM_FORMAT (wmsdkidl.h)
description: The WMT_WEBSTREAM_FORMAT structure contains information about a Web stream. This structure is used as the pbFormat member of the WM_MEDIA_TYPE structure for Web streams.
helpviewer_keywords: ["WMT_WEBSTREAM_FORMAT","WMT_WEBSTREAM_FORMAT structure [windows Media Format]","wmformat.wmt_webstream_format","wmsdkidl/WMT_WEBSTREAM_FORMAT"]
old-location: wmformat\wmt_webstream_format.htm
tech.root: wmformat
ms.assetid: 3a392b33-6c2b-4465-86b4-6614940d7383
ms.date: 12/05/2018
ms.keywords: WMT_WEBSTREAM_FORMAT, WMT_WEBSTREAM_FORMAT structure [windows Media Format], wmformat.wmt_webstream_format, wmsdkidl/WMT_WEBSTREAM_FORMAT
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: WMT_WEBSTREAM_FORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WMT_WEBSTREAM_FORMAT
 - wmsdkidl/_WMT_WEBSTREAM_FORMAT
 - WMT_WEBSTREAM_FORMAT
 - wmsdkidl/WMT_WEBSTREAM_FORMAT
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
 - WMT_WEBSTREAM_FORMAT
---

# WMT_WEBSTREAM_FORMAT structure


## -description

The <b>WMT_WEBSTREAM_FORMAT</b> structure contains information about a Web stream. This structure is used as the <b>pbFormat</b> member of the <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type">WM_MEDIA_TYPE</a> structure for Web streams.

## -struct-fields

### -field cbSize

<b>WORD</b> containing the size of the structure, in bytes.

### -field cbSampleHeaderFixedData

<b>WORD</b> containing the size of Web stream sample header, in bytes.

### -field wVersion

<b>WORD</b> containing the version number. Set to 1 for streams created with the Windows Media Format 9 Series SDK.

### -field wReserved

<b>WORD</b>. Reserved.

## -see-also

<a href="/windows/desktop/wmformat/structures">Structures</a>