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



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

