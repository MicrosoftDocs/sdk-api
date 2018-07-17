---
UID: NE:wmsdkidl.WMT_CODEC_INFO_TYPE
title: WMT_CODEC_INFO_TYPE
author: windows-sdk-content
description: The WMT_CODEC_INFO_TYPE enumeration type defines the broad categories of codecs supported by this SDK.
old-location: wmformat\wmt_codec_info_type.htm
old-project: wmformat
ms.assetid: 31fcaa84-1b7e-407c-95dc-bf13263b788a
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: WMT_CODECINFO_AUDIO, WMT_CODECINFO_UNKNOWN, WMT_CODECINFO_VIDEO, WMT_CODEC_INFO_TYPE, WMT_CODEC_INFO_TYPE enumeration [windows Media Format], wmformat.wmt_codec_info_type, wmsdkidl/WMT_CODECINFO_AUDIO, wmsdkidl/WMT_CODECINFO_UNKNOWN, wmsdkidl/WMT_CODECINFO_VIDEO, wmsdkidl/WMT_CODEC_INFO_TYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: WMT_CODEC_INFO_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WMT_CODEC_INFO_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WMT_CODEC_INFO_TYPE enumeration


## -description



The <b>WMT_CODEC_INFO_TYPE</b> enumeration type defines the broad categories of codecs supported by this SDK.




## -enum-fields




### -field WMT_CODECINFO_AUDIO

Audio codec.


### -field WMT_CODECINFO_VIDEO

Video codec.


### -field WMT_CODECINFO_UNKNOWN

Codec of an unknown type.


## -remarks



This type is used when adding or retrieving the codecs used in a file using <a href="https://msdn.microsoft.com/685eaf9e-6cc8-4c38-be34-afa4b504a326">IWMHeaderInfo2::GetCodecInfo</a> and <a href="https://msdn.microsoft.com/4c5bc019-e4bb-419b-91ce-779fd36d7b4c">IWMHeaderInfo3::AddCodecInfo</a>. When enumerating codecs with the methods of <b>IWMCodecInfo</b>, <b>IWMCodecInfo2</b>, and <b>IWMCodecInfo3</b>, you do not use this type. Those methods use the major media type GUIDs instead.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>
 

 

