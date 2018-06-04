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

# _WMWriterStatistics structure


## -description



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




<a href="https://msdn.microsoft.com/005c2039-e821-42ab-bead-1bf40f2ab171">IWMWriterAdvanced::GetStatistics</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

