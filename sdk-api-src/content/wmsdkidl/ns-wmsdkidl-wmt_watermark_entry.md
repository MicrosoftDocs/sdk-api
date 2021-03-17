---
UID: NS:wmsdkidl.__WMT_WATERMARK_ENTRY
title: WMT_WATERMARK_ENTRY (wmsdkidl.h)
description: The WMT_WATERMARK_ENTRY structure contains information describing a watermarking system.
helpviewer_keywords: ["WMT_WATERMARK_ENTRY","WMT_WATERMARK_ENTRY structure [windows Media Format]","structure [windows Media Format]","wmformat.wmt_watermark_entry","wmsdkidl/WMT_WATERMARK_ENTRY"]
old-location: wmformat\wmt_watermark_entry.htm
tech.root: wmformat
ms.assetid: 9b7b78e1-cf28-4b7a-8a12-e9d19cec17c4
ms.date: 12/05/2018
ms.keywords: WMT_WATERMARK_ENTRY, WMT_WATERMARK_ENTRY structure [windows Media Format], structure [windows Media Format], wmformat.wmt_watermark_entry, wmsdkidl/WMT_WATERMARK_ENTRY
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
req.typenames: WMT_WATERMARK_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __WMT_WATERMARK_ENTRY
 - wmsdkidl/__WMT_WATERMARK_ENTRY
 - WMT_WATERMARK_ENTRY
 - wmsdkidl/WMT_WATERMARK_ENTRY
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
 - WMT_WATERMARK_ENTRY
---

# WMT_WATERMARK_ENTRY structure


## -description

The <b>WMT_WATERMARK_ENTRY</b> structure contains information describing a watermarking system.

## -struct-fields

### -field wmetType

A value from the <b>WMT_WATERMARK_ENTRY_TYPE</b> enumeration type specifying the type of watermarking system.

### -field clsid

GUID value identifying the watermarking system.

### -field cbDisplayName

The size of display name in wide characters.

### -field pwszDisplayName

Pointer to a wide-character null-terminated string containing the display name.

## -see-also

<a href="/windows/desktop/wmformat/structures">Structures</a>