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

# linemonitortone_tag structure


## -description


The 
<b>LINEMONITORTONE</b> structure describes a tone to be monitored. This is used as an entry in an array. The 
<a href="https://msdn.microsoft.com/47fe21f2-7896-4ccf-8c26-33430b2081ac">lineMonitorTones</a> and 
<a href="https://msdn.microsoft.com/8b16dda3-bcb4-4a89-b2e5-b9330be3eb01">TSPI_lineMonitorTones</a> functions use this structure.


## -struct-fields




### -field dwAppSpecific

Used by the application for tagging the tone. When this tone is detected, the value of the <b>dwAppSpecific</b> member is passed back to the application.


### -field dwDuration

Duration of time during which the tone should be present before a detection is made, in milliseconds.


### -field dwFrequency1

First frequency of the tone, in hertz.


### -field dwFrequency2

Second frequency of the tone, in hertz.


### -field dwFrequency3

Third frequency of the tone, in hertz. If fewer than three frequencies are needed in the tone, a value of 0 should be used for the unused frequencies. A tone with all three frequencies set to zero is interpreted as silence and can be use for silence detection.


## -remarks



This structure may not be extended.

The 
<b>LINEMONITORTONE</b> structure defines a tone for the purpose of detection. An array of tones is passed to the 
<a href="https://msdn.microsoft.com/47fe21f2-7896-4ccf-8c26-33430b2081ac">lineMonitorTones</a> function which monitors these tones and sends a LINE_MONITORTONE message to the application when a detection is made.

A tone with all frequencies set to zero corresponds to silence. An application can thus monitor the call's information stream for silence.




## -see-also




<a href="https://msdn.microsoft.com/ffdca615-5341-4f02-bb38-b8133cd9477d">LINE_MONITORTONE</a>



<a href="https://msdn.microsoft.com/8b16dda3-bcb4-4a89-b2e5-b9330be3eb01">TSPI_lineMonitorTones</a>



<a href="https://msdn.microsoft.com/47fe21f2-7896-4ccf-8c26-33430b2081ac">lineMonitorTones</a>
 

 

