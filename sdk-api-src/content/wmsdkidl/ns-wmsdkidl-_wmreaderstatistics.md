---
UID: NS:wmsdkidl._WMReaderStatistics
title: "_WMReaderStatistics"
author: windows-sdk-content
description: The WM_READER_STATISTICS structure describes the performance of a reading operation.
old-location: wmformat\wm_reader_statistics.htm
tech.root: wmformat
ms.assetid: 30e58e9b-5247-4d9a-91dc-fd137d8f5613
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: WM_READER_STATISTICS, WM_READER_STATISTICS structure [windows Media Format], _WMReaderStatistics, wmformat.wm_reader_statistics, wmsdkidl/WM_READER_STATISTICS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WM_READER_STATISTICS
product: Windows
targetos: Windows
req.typenames: WM_READER_STATISTICS
req.redist: 
---

# _WMReaderStatistics structure


## -description



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




<a href="https://msdn.microsoft.com/9ed2a3fe-c31d-42fc-9ee9-27dd9aef7e06">IWMReaderAdvanced::GetStatistics</a>



<a href="https://msdn.microsoft.com/118ef278-ca4f-4c30-9633-a2d851f5c758">Structures</a>
 

 

