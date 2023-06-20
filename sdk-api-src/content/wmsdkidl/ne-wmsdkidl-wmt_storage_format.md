---
UID: NE:wmsdkidl.tagWMT_STORAGE_FORMAT
title: WMT_STORAGE_FORMAT (wmsdkidl.h)
description: The WMT_STORAGE_FORMAT enumeration type defines the file types that can be manipulated with this SDK.
helpviewer_keywords: ["WMT_STORAGE_FORMAT","WMT_STORAGE_FORMAT enumeration [windows Media Format]","WMT_Storage_Format_MP3","WMT_Storage_Format_V1","wmformat.wmt_storage_format","wmsdkidl/WMT_STORAGE_FORMAT","wmsdkidl/WMT_Storage_Format_MP3","wmsdkidl/WMT_Storage_Format_V1"]
old-location: wmformat\wmt_storage_format.htm
tech.root: wmformat
ms.assetid: 49f49ca8-8953-47a6-97c3-fd011d5f88cd
ms.date: 4/26/2023
ms.keywords: WMT_STORAGE_FORMAT, WMT_STORAGE_FORMAT enumeration [windows Media Format], WMT_Storage_Format_MP3, WMT_Storage_Format_V1, wmformat.wmt_storage_format, wmsdkidl/WMT_STORAGE_FORMAT, wmsdkidl/WMT_Storage_Format_MP3, wmsdkidl/WMT_Storage_Format_V1
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
req.typenames: WMT_STORAGE_FORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWMT_STORAGE_FORMAT
 - wmsdkidl/tagWMT_STORAGE_FORMAT
 - WMT_STORAGE_FORMAT
 - wmsdkidl/WMT_STORAGE_FORMAT
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
 - WMT_STORAGE_FORMAT
---

# WMT_STORAGE_FORMAT enumeration


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WMT_STORAGE_FORMAT</b> enumeration type defines the file types that can be manipulated with this SDK.

## -enum-fields

### -field WMT_Storage_Format_MP3:0

The file is encoded in MP3 format.

### -field WMT_Storage_Format_V1

The file is encoded in Windows Media Format.

## -remarks

Storage format MP3 is supported for reading, but not writing.

## -see-also

<a href="/windows/desktop/wmformat/enumeration-types">Enumeration Types</a>
