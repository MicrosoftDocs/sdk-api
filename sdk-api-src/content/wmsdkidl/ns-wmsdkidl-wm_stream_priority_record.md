---
UID: NS:wmsdkidl._WMStreamPrioritizationRecord
title: WM_STREAM_PRIORITY_RECORD (wmsdkidl.h)
description: The WM_STREAM_PRIORITY_RECORD structure contains a stream number and specifies whether delivery of that stream is mandatory.
helpviewer_keywords: ["WM_STREAM_PRIORITY_RECORD","WM_STREAM_PRIORITY_RECORD structure [windows Media Format]","wmformat.wm_stream_priority_record","wmsdkidl/WM_STREAM_PRIORITY_RECORD"]
old-location: wmformat\wm_stream_priority_record.htm
tech.root: wmformat
ms.assetid: 43c9370c-cd43-4dd0-8258-d6dbdb98f1de
ms.date: 4/26/2023
ms.keywords: WM_STREAM_PRIORITY_RECORD, WM_STREAM_PRIORITY_RECORD structure [windows Media Format], wmformat.wm_stream_priority_record, wmsdkidl/WM_STREAM_PRIORITY_RECORD
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
req.typenames: WM_STREAM_PRIORITY_RECORD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WMStreamPrioritizationRecord
 - wmsdkidl/_WMStreamPrioritizationRecord
 - WM_STREAM_PRIORITY_RECORD
 - wmsdkidl/WM_STREAM_PRIORITY_RECORD
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
 - WM_STREAM_PRIORITY_RECORD
---

# WM_STREAM_PRIORITY_RECORD structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WM_STREAM_PRIORITY_RECORD</b> structure contains a stream number and specifies whether delivery of that stream is mandatory.

## -struct-fields

### -field wStreamNumber

<b>WORD</b> containing the stream number.

### -field fMandatory

Flag indicating whether the listed stream is mandatory. Mandatory streams will not be dropped regardless of their position in the priority list.

## -remarks

<b>WM_STREAM_PRIORITY_RECORD</b> is used in an array by the <b>IWMStreamPrioritization</b> interface. Each member of the array specifies a stream; the lower the element number in the array, the higher the priority of the stream.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization">IWMStreamPrioritization Interface</a>



<a href="/windows/desktop/wmformat/structures">Structures</a>