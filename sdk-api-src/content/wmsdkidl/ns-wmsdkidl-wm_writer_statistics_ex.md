---
UID: NS:wmsdkidl._WMWriterStatisticsEx
title: WM_WRITER_STATISTICS_EX (wmsdkidl.h)
description: The WM_WRITER_STATISTICS_EX structure is used by IWMWriterAdvanced3::GetStatisticsEx to obtain extended writer statistics.
helpviewer_keywords: ["WM_WRITER_STATISTICS_EX","WM_WRITER_STATISTICS_EX structure [windows Media Format]","wmformat.wm_writer_statistics_ex","wmsdkidl/WM_WRITER_STATISTICS_EX"]
old-location: wmformat\wm_writer_statistics_ex.htm
tech.root: wmformat
ms.assetid: f98a5934-968e-4c74-9fd2-f824ad77692c
ms.date: 12/05/2018
ms.keywords: WM_WRITER_STATISTICS_EX, WM_WRITER_STATISTICS_EX structure [windows Media Format], wmformat.wm_writer_statistics_ex, wmsdkidl/WM_WRITER_STATISTICS_EX
f1_keywords:
- wmsdkidl/WM_WRITER_STATISTICS_EX
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Wmsdkidl.h
api_name:
- WM_WRITER_STATISTICS_EX
targetos: Windows
req.typenames: WM_WRITER_STATISTICS_EX
req.redist: 
ms.custom: 19H1
---

# WM_WRITER_STATISTICS_EX structure


## -description



The <b>WM_WRITER_STATISTICS_EX</b> structure is used by <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex">IWMWriterAdvanced3::GetStatisticsEx</a> to obtain extended writer statistics.




## -struct-fields




### -field dwBitratePlusOverhead

<b>DWORD</b> containing the bit rate plus any overhead.


### -field dwCurrentSampleDropRateInQueue

<b>DWORD</b> containing the current rate at which samples are dropped in the queue in order to reduce demands on the CPU.


### -field dwCurrentSampleDropRateInCodec

<b>DWORD</b> containing the current rate at which samples are dropped in the codec. Samples can be dropped when they contain little new data. To prevent this from happening, call <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting">IWMWriterAdvanced2::SetInputSetting</a> to set the g_wszFixedFrameRate setting to <b>TRUE</b>.


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

Basic writer statistics are contained within a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics">WM_WRITER_STATISTICS</a> structure and must be obtained by calling <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics">IWMWriterAdvanced::GetStatistics</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/structures">Structures</a>
 

 

