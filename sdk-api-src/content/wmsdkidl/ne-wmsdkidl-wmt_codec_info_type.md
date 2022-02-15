---
UID: NE:wmsdkidl.WMT_CODEC_INFO_TYPE
title: WMT_CODEC_INFO_TYPE (wmsdkidl.h)
description: The WMT_CODEC_INFO_TYPE enumeration type defines the broad categories of codecs supported by this SDK.
helpviewer_keywords: ["WMT_CODECINFO_AUDIO","WMT_CODECINFO_UNKNOWN","WMT_CODECINFO_VIDEO","WMT_CODEC_INFO_TYPE","WMT_CODEC_INFO_TYPE enumeration [windows Media Format]","wmformat.wmt_codec_info_type","wmsdkidl/WMT_CODECINFO_AUDIO","wmsdkidl/WMT_CODECINFO_UNKNOWN","wmsdkidl/WMT_CODECINFO_VIDEO","wmsdkidl/WMT_CODEC_INFO_TYPE"]
old-location: wmformat\wmt_codec_info_type.htm
tech.root: wmformat
ms.assetid: 31fcaa84-1b7e-407c-95dc-bf13263b788a
ms.date: 12/05/2018
ms.keywords: WMT_CODECINFO_AUDIO, WMT_CODECINFO_UNKNOWN, WMT_CODECINFO_VIDEO, WMT_CODEC_INFO_TYPE, WMT_CODEC_INFO_TYPE enumeration [windows Media Format], wmformat.wmt_codec_info_type, wmsdkidl/WMT_CODECINFO_AUDIO, wmsdkidl/WMT_CODECINFO_UNKNOWN, wmsdkidl/WMT_CODECINFO_VIDEO, wmsdkidl/WMT_CODEC_INFO_TYPE
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.typenames: WMT_CODEC_INFO_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMT_CODEC_INFO_TYPE
 - wmsdkidl/WMT_CODEC_INFO_TYPE
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
 - WMT_CODEC_INFO_TYPE
---

# WMT_CODEC_INFO_TYPE enumeration


## -description

The <b>WMT_CODEC_INFO_TYPE</b> enumeration type defines the broad categories of codecs supported by this SDK.

## -enum-fields

### -field WMT_CODECINFO_AUDIO:0

Audio codec.

### -field WMT_CODECINFO_VIDEO:1

Video codec.

### -field WMT_CODECINFO_UNKNOWN:0xffffffff

Codec of an unknown type.

## -remarks

This type is used when adding or retrieving the codecs used in a file using <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo">IWMHeaderInfo2::GetCodecInfo</a> and <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo">IWMHeaderInfo3::AddCodecInfo</a>. When enumerating codecs with the methods of <b>IWMCodecInfo</b>, <b>IWMCodecInfo2</b>, and <b>IWMCodecInfo3</b>, you do not use this type. Those methods use the major media type GUIDs instead.

## -see-also

<a href="/windows/desktop/wmformat/enumeration-types">Enumeration Types</a>
