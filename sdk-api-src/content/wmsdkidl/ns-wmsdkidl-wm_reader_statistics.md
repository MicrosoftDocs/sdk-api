---
UID: NS:wmsdkidl._WMReaderStatistics
title: WM_READER_STATISTICS (wmsdkidl.h)
description: The WM_READER_STATISTICS structure describes the performance of a reading operation.
helpviewer_keywords: ["WM_READER_STATISTICS","WM_READER_STATISTICS structure [windows Media Format]","wmformat.wm_reader_statistics","wmsdkidl/WM_READER_STATISTICS"]
old-location: wmformat\wm_reader_statistics.htm
tech.root: wmformat
ms.assetid: 30e58e9b-5247-4d9a-91dc-fd137d8f5613
ms.date: 4/26/2023
ms.keywords: WM_READER_STATISTICS, WM_READER_STATISTICS structure [windows Media Format], wmformat.wm_reader_statistics, wmsdkidl/WM_READER_STATISTICS
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
req.typenames: WM_READER_STATISTICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WMReaderStatistics
 - wmsdkidl/_WMReaderStatistics
 - WM_READER_STATISTICS
 - wmsdkidl/WM_READER_STATISTICS
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
 - WM_READER_STATISTICS
---

# WM_READER_STATISTICS structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WM_READER_STATISTICS</b> structure describes the performance of a reading operation.

## -struct-fields

### -field cbSize

The size of the <b>WM_READER_STATISTICS</b> structure, in bytes.

### -field dwBandwidth

<b>DWORD</b> containing the bandwidth, in bits per second.

### -field cPacketsReceived

Count of packets received.

### -field cPacketsRecovered

Count of lost packets which were recovered. This value is only relevant during network playback.

### -field cPacketsLost

Count of lost packets which were not recovered. This value is only relevant during network playback.

### -field wQuality

<b>WORD</b> containing the quality, which is the percentage of total packets that were received.

## -remarks

You must set the <b>cbSize</b> member manually before using this structure. It should always be set to sizeof(<b>WM_READER_STATISTICS</b>).

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics">IWMReaderAdvanced::GetStatistics</a>



<a href="/windows/desktop/wmformat/structures">Structures</a>