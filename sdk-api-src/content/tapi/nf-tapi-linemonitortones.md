---
UID: NF:tapi.lineMonitorTones
title: lineMonitorTones function
author: windows-sdk-content
description: The lineMonitorTones function enables and disables the detection of inband tones on the call. Each time a specified tone is detected, a message is sent to the application.
old-location: tapi2\linemonitortones.htm
tech.root: tapi
ms.assetid: 47fe21f2-7896-4ccf-8c26-33430b2081ac
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "_tapi2_linemonitortones, lineMonitorTones, lineMonitorTones function [TAPI 2.2], tapi/lineMonitorTones, tapi2.linemonitortones"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineMonitorTones
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineMonitorTones function


## -description


The 
<b>lineMonitorTones</b> function enables and disables the detection of inband tones on the call. Each time a specified tone is detected, a message is sent to the application.


## -parameters




### -param hCall

Handle to the call on whose voice channel tones are to be monitored. The call state of <i>hCall</i> can be any state except <i>idle</i>.


### -param lpToneList

List of tones to be monitored. This parameter is of type 
<a href="https://msdn.microsoft.com/f2d37591-2f1e-458f-b4d4-ab63eb31d33a">LINEMONITORTONE</a>. Each tone in this list has an application-defined tag field that is used to identify individual tones in the list to report a tone detection. Tone monitoring in progress is canceled or changed by calling this operation with either <b>NULL</b> for <i>lpToneList</i> or with another tone list.


### -param dwNumEntries

Number of entries in <i>lpToneList</i>. This parameter is ignored if <i>lpToneList</i> is <b>NULL</b>.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_INVALCALLSTATE, LINEERR_INVALPOINTER, LINEERR_INVALTONE, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_OPERATIONUNAVAIL, LINEERR_RESOURCEUNAVAIL, LINEERR_UNINITIALIZED.




## -remarks



This function succeeds if tone monitoring has been correctly initiated, not when tone monitoring has terminated. Tone monitoring remains in effect until it is explicitly disabled by calling 
<b>lineMonitorTones</b> with another tone list (or <b>NULL</b>), until the call transitions to <i>idle</i>, or when the application deallocates its call handle for the call.

Although this function can be invoked in any call state, tones can typically only be detected while the call is in the <i>connected</i> state. Tone detection typically requires computational resources. Depending on the service provider and other activities that compete for such resources, the number of tones that can be detected can vary over time. Also, an equivalent amount of resources can be consumed for monitoring a single triple frequency tone versus three single frequency tones. If resources are overcommitted, the LINEERR_RESOURCEUNAVAIL error is returned.

The 
<b>lineMonitorTones</b> function is also used to detect silence. Silence is specified as a tone with a frequency of zero.

Monitoring of tones on a conference call applies only to the <i>hConfCall</i>, not to the individual participating calls

If the LINEERR_INVALPOINTER error value is returned, the specified <i>lpToneList</i> parameter is invalid or the value specified by the <i>dwNumEntries</i> parameter is too large.




## -see-also




<a href="https://msdn.microsoft.com/f2d37591-2f1e-458f-b4d4-ab63eb31d33a">LINEMONITORTONE</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 

