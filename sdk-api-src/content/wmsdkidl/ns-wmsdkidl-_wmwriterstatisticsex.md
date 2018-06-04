---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _WMWriterStatisticsEx structure


## -description



The <b>WM_WRITER_STATISTICS_EX</b> structure is used by <a href="https://msdn.microsoft.com/3ea41491-409c-42b7-a4b2-f0d7c222c299">IWMWriterAdvanced3::GetStatisticsEx</a> to obtain extended writer statistics.




## -struct-fields




### -field dwBitratePlusOverhead

<b>DWORD</b> containing the bit rate plus any overhead.


### -field dwCurrentSampleDropRateInQueue

<b>DWORD</b> containing the current rate at which samples are dropped in the queue in order to reduce demands on the CPU.


### -field dwCurrentSampleDropRateInCodec

<b>DWORD</b> containing the current rate at which samples are dropped in the codec. Samples can be dropped when they contain little new data. To prevent this from happening, call <a href="https://msdn.microsoft.com/a920bfe8-1f95-4957-b6c4-9749d5e10ee3">IWMWriterAdvanced2::SetInputSetting</a> to set the g_wszFixedFrameRate setting to <b>TRUE</b>.


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

Basic writer statistics are contained within a <a href="https://msdn.microsoft.com/907711c9-2ae1-4049-afd8-768912778e37">WM_WRITER_STATISTICS</a> structure and must be obtained by calling <a href="https://msdn.microsoft.com/005c2039-e821-42ab-bead-1bf40f2ab171">IWMWriterAdvanced::GetStatistics</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

