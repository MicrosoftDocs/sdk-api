---
UID: NS:tapi.linemonitortone_tag
title: linemonitortone_tag
author: windows-sdk-content
description: The LINEMONITORTONE structure describes a tone to be monitored. This is used as an entry in an array. The lineMonitorTones and TSPI_lineMonitorTones functions use this structure.
old-location: tapi2\linemonitortone_str.htm
old-project: tapi
ms.assetid: f2d37591-2f1e-458f-b4d4-ab63eb31d33a
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: "*LPLINEMONITORTONE, LINEMONITORTONE, LINEMONITORTONE structure [TAPI 2.2], LPLINEMONITORTONE, LPLINEMONITORTONE structure pointer [TAPI 2.2], _tapi2_linemonitortone_str, linemonitortone_tag, tapi/LINEMONITORTONE, tapi/LPLINEMONITORTONE, tapi2.linemonitortone_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tapi.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: LINEMONITORTONE, *LPLINEMONITORTONE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINEMONITORTONE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

