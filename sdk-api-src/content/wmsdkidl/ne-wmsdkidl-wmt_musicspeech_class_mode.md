---
UID: NE:wmsdkidl.tagWMT_MUSICSPEECH_CLASS_MODE
title: WMT_MUSICSPEECH_CLASS_MODE (wmsdkidl.h)
description: The WMT_MUSICSPEECH_CLASS_MODE enumeration type defines the types of compression supported by the Windows Media Audio 9 Voice codec.
helpviewer_keywords: ["WMT_MS_CLASS_MIXED","WMT_MS_CLASS_MUSIC","WMT_MS_CLASS_SPEECH","WMT_MUSICSPEECH_CLASS_MODE","WMT_MUSICSPEECH_CLASS_MODE enumeration [windows Media Format]","wmformat.wmt_musicspeech_class_mode","wmsdkidl/WMT_MS_CLASS_MIXED","wmsdkidl/WMT_MS_CLASS_MUSIC","wmsdkidl/WMT_MS_CLASS_SPEECH","wmsdkidl/WMT_MUSICSPEECH_CLASS_MODE"]
old-location: wmformat\wmt_musicspeech_class_mode.htm
tech.root: wmformat
ms.assetid: 9ca744a1-1d85-4609-8f5f-d074e46cef45
ms.date: 4/26/2023
ms.keywords: WMT_MS_CLASS_MIXED, WMT_MS_CLASS_MUSIC, WMT_MS_CLASS_SPEECH, WMT_MUSICSPEECH_CLASS_MODE, WMT_MUSICSPEECH_CLASS_MODE enumeration [windows Media Format], wmformat.wmt_musicspeech_class_mode, wmsdkidl/WMT_MS_CLASS_MIXED, wmsdkidl/WMT_MS_CLASS_MUSIC, wmsdkidl/WMT_MS_CLASS_SPEECH, wmsdkidl/WMT_MUSICSPEECH_CLASS_MODE
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
req.typenames: WMT_MUSICSPEECH_CLASS_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWMT_MUSICSPEECH_CLASS_MODE
 - wmsdkidl/tagWMT_MUSICSPEECH_CLASS_MODE
 - WMT_MUSICSPEECH_CLASS_MODE
 - wmsdkidl/WMT_MUSICSPEECH_CLASS_MODE
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
 - WMT_MUSICSPEECH_CLASS_MODE
---

# WMT_MUSICSPEECH_CLASS_MODE enumeration


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WMT_MUSICSPEECH_CLASS_MODE</b> enumeration type defines the types of compression supported by the Windows Media Audio 9 Voice codec.

## -enum-fields

### -field WMT_MS_CLASS_MUSIC:0

Not currently supported. Do not use.

### -field WMT_MS_CLASS_SPEECH:1

Compression optimized for speech.

### -field WMT_MS_CLASS_MIXED:2

Compression optimized for a mixture of music and speech.

## -see-also

<a href="/windows/desktop/wmformat/enumeration-types">Enumeration Types</a>
