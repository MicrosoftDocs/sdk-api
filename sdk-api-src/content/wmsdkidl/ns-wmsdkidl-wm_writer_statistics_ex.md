---
UID: NS:wmsdkidl._WMWriterStatisticsEx
title: WM_WRITER_STATISTICS_EX (wmsdkidl.h)
description: The WM_WRITER_STATISTICS_EX structure is used by IWMWriterAdvanced3::GetStatisticsEx to obtain extended writer statistics.
helpviewer_keywords: ["WM_WRITER_STATISTICS_EX","WM_WRITER_STATISTICS_EX structure [windows Media Format]","wmformat.wm_writer_statistics_ex","wmsdkidl/WM_WRITER_STATISTICS_EX"]
old-location: wmformat\wm_writer_statistics_ex.htm
tech.root: wmformat
ms.assetid: f98a5934-968e-4c74-9fd2-f824ad77692c
ms.date: 4/26/2023
ms.keywords: WM_WRITER_STATISTICS_EX, WM_WRITER_STATISTICS_EX structure [windows Media Format], wmformat.wm_writer_statistics_ex, wmsdkidl/WM_WRITER_STATISTICS_EX
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
req.typenames: WM_WRITER_STATISTICS_EX
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WMWriterStatisticsEx
 - wmsdkidl/_WMWriterStatisticsEx
 - WM_WRITER_STATISTICS_EX
 - wmsdkidl/WM_WRITER_STATISTICS_EX
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
 - WM_WRITER_STATISTICS_EX
---

# WM_WRITER_STATISTICS_EX structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WM_WRITER_STATISTICS_EX</b> structure is used by <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex">IWMWriterAdvanced3::GetStatisticsEx</a> to obtain extended writer statistics.

## -struct-fields

### -field dwBitratePlusOverhead

<b>DWORD</b> containing the bit rate plus any overhead.

### -field dwCurrentSampleDropRateInQueue

<b>DWORD</b> containing the current rate at which samples are dropped in the queue in order to reduce demands on the CPU.

### -field dwCurrentSampleDropRateInCodec

<b>DWORD</b> containing the current rate at which samples are dropped in the codec. Samples can be dropped when they contain little new data. To prevent this from happening, call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting">IWMWriterAdvanced2::SetInputSetting</a> to set the g_wszFixedFrameRate setting to <b>TRUE</b>.

### -field dwCurrentSampleDropRateInMultiplexer

<b>DWORD</b> containing the current rate at which samples are dropped in the multiplexer because they arrived late or overflowed the buffer window.

### -field dwTotalSampleDropsInQueue

<b>DWORD</b> containing the total number of samples dropped in the queue.

### -field dwTotalSampleDropsInCodec

<b>DWORD</b> containing the total number of samples dropped in the codec.

### -field dwTotalSampleDropsInMultiplexer

<b>DWORD</b> containing the total number of samples dropped in the multiplexer.

## -remarks

Sample rates are given in kilohertz.

Basic writer statistics are contained within a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics">WM_WRITER_STATISTICS</a> structure and must be obtained by calling <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics">IWMWriterAdvanced::GetStatistics</a>.

## -see-also

<a href="/windows/desktop/wmformat/structures">Structures</a>