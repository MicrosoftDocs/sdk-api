---
UID: NF:tapi.lineMonitorTones
title: lineMonitorTones function (tapi.h)
description: The lineMonitorTones function enables and disables the detection of inband tones on the call. Each time a specified tone is detected, a message is sent to the application.
helpviewer_keywords: ["_tapi2_linemonitortones","lineMonitorTones","lineMonitorTones function [TAPI 2.2]","tapi/lineMonitorTones","tapi2.linemonitortones"]
old-location: tapi2\linemonitortones.htm
tech.root: tapi3
ms.assetid: 47fe21f2-7896-4ccf-8c26-33430b2081ac
ms.date: 12/05/2018
ms.keywords: _tapi2_linemonitortones, lineMonitorTones, lineMonitorTones function [TAPI 2.2], tapi/lineMonitorTones, tapi2.linemonitortones
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineMonitorTones
 - tapi/lineMonitorTones
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineMonitorTones
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
<a href="/windows/desktop/api/tapi/ns-tapi-linemonitortone">LINEMONITORTONE</a>. Each tone in this list has an application-defined tag field that is used to identify individual tones in the list to report a tone detection. Tone monitoring in progress is canceled or changed by calling this operation with either <b>NULL</b> for <i>lpToneList</i> or with another tone list.

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

<a href="/windows/desktop/api/tapi/ns-tapi-linemonitortone">LINEMONITORTONE</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>