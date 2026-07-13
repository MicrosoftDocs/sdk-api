---
UID: NS:wmsdkidl._WMWriterStatistics
title: WM_WRITER_STATISTICS (wmsdkidl.h)
description: The WM_WRITER_STATISTICS structure describes the performance of a writing operation.
helpviewer_keywords: ["WM_WRITER_STATISTICS","WM_WRITER_STATISTICS structure [windows Media Format]","wmformat.wm_writer_statistics","wmsdkidl/WM_WRITER_STATISTICS"]
old-location: wmformat\wm_writer_statistics.htm
tech.root: wmformat
ms.assetid: 907711c9-2ae1-4049-afd8-768912778e37
ms.date: 4/26/2023
ms.keywords: WM_WRITER_STATISTICS, WM_WRITER_STATISTICS structure [windows Media Format], wmformat.wm_writer_statistics, wmsdkidl/WM_WRITER_STATISTICS
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
req.typenames: WM_WRITER_STATISTICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WMWriterStatistics
 - wmsdkidl/_WMWriterStatistics
 - WM_WRITER_STATISTICS
 - wmsdkidl/WM_WRITER_STATISTICS
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
 - WM_WRITER_STATISTICS
---

# WM_WRITER_STATISTICS structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WM_WRITER_STATISTICS</b> structure describes the performance of a writing operation.

## -struct-fields

### -field qwSampleCount

<b>QWORD</b> containing the sample count.

### -field qwByteCount

<b>QWORD</b> containing the byte count.

### -field qwDroppedSampleCount

<b>QWORD</b> containing the dropped sample count.

### -field qwDroppedByteCount

<b>QWORD</b> containing the dropped byte count.

### -field dwCurrentBitrate

<b>DWORD</b> containing the current bit rate.

### -field dwAverageBitrate

<b>DWORD</b> containing the average bit rate.

### -field dwExpectedBitrate

<b>DWORD</b> containing the expected bit rate.

### -field dwCurrentSampleRate

<b>DWORD</b> containing the current sample rate.

### -field dwAverageSampleRate

<b>DWORD</b> containing the average sample rate.

### -field dwExpectedSampleRate

<b>DWORD</b> containing the expected sample rate.

## -remarks

Sample rates are specified in kilohertz. For instance, a sample rate of 8 indicates 8000 samples per second.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics">IWMWriterAdvanced::GetStatistics</a>



<a href="/windows/desktop/wmformat/structures">Structures</a>