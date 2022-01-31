---
UID: NE:wmsdkidl.tagWMT_FILESINK_MODE
title: WMT_FILESINK_MODE (wmsdkidl.h)
description: The WMT_FILESINK_MODE enumeration type defines the types of input accepted by the file sink.
helpviewer_keywords: ["WMT_FILESINK_MODE","WMT_FILESINK_MODE enumeration [windows Media Format]","WMT_FM_FILESINK_DATA_UNITS","WMT_FM_FILESINK_UNBUFFERED","WMT_FM_SINGLE_BUFFERS","wmformat.wmt_filesink_mode","wmsdkidl/WMT_FILESINK_MODE","wmsdkidl/WMT_FM_FILESINK_DATA_UNITS","wmsdkidl/WMT_FM_FILESINK_UNBUFFERED","wmsdkidl/WMT_FM_SINGLE_BUFFERS"]
old-location: wmformat\wmt_filesink_mode.htm
tech.root: wmformat
ms.assetid: 27846996-1957-4b19-91da-feeef477b06a
ms.date: 12/05/2018
ms.keywords: WMT_FILESINK_MODE, WMT_FILESINK_MODE enumeration [windows Media Format], WMT_FM_FILESINK_DATA_UNITS, WMT_FM_FILESINK_UNBUFFERED, WMT_FM_SINGLE_BUFFERS, wmformat.wmt_filesink_mode, wmsdkidl/WMT_FILESINK_MODE, wmsdkidl/WMT_FM_FILESINK_DATA_UNITS, wmsdkidl/WMT_FM_FILESINK_UNBUFFERED, wmsdkidl/WMT_FM_SINGLE_BUFFERS
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
req.typenames: WMT_FILESINK_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWMT_FILESINK_MODE
 - wmsdkidl/tagWMT_FILESINK_MODE
 - WMT_FILESINK_MODE
 - wmsdkidl/WMT_FILESINK_MODE
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
 - WMT_FILESINK_MODE
---

# WMT_FILESINK_MODE enumeration


## -description

The <b>WMT_FILESINK_MODE</b> enumeration type defines the types of input accepted by the file sink.

## -enum-fields

### -field WMT_FM_SINGLE_BUFFERS:0x1

The file sink accepts normal buffers through calls to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwritersink-ondataunit">IWMWriterSink::OnDataUnit</a>. This is the default behavior.

### -field WMT_FM_FILESINK_DATA_UNITS:0x2

The file sink accepts data as <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_filesink_data_unit">WMT_FILESINK_DATA_UNIT</a> structures delivered by <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-ondataunitex">IWMWriterFileSink3::OnDataUnitEx</a>.

### -field WMT_FM_FILESINK_UNBUFFERED:0x4

The file sink accepts unbuffered data. A call to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-setunbufferedio">IWMWriterFileSink3::SetUnbufferedIO</a> will succeed.

## -see-also

<a href="/windows/desktop/wmformat/enumeration-types">Enumeration Types</a>
