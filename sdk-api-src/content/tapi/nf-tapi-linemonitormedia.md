---
UID: NF:tapi.lineMonitorMedia
title: lineMonitorMedia function (tapi.h)
description: The lineMonitorMedia function enables and disables the detection of media types (modes) on the specified call. When a media type is detected, a message is sent to the application. For more information, see ITLegacyCallMediaControl::MonitorMedia.
helpviewer_keywords: ["_tapi2_linemonitormedia","lineMonitorMedia","lineMonitorMedia function [TAPI 2.2]","tapi/lineMonitorMedia","tapi2.linemonitormedia"]
old-location: tapi2\linemonitormedia.htm
tech.root: tapi3
ms.assetid: d79a5469-2248-466b-a5ca-32a568b135d2
ms.date: 12/05/2018
ms.keywords: _tapi2_linemonitormedia, lineMonitorMedia, lineMonitorMedia function [TAPI 2.2], tapi/lineMonitorMedia, tapi2.linemonitormedia
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
 - lineMonitorMedia
 - tapi/lineMonitorMedia
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
 - lineMonitorMedia
---

# lineMonitorMedia function


## -description

The 
<b>lineMonitorMedia</b> function enables and disables the detection of media types (modes) on the specified call. When a media type is detected, a message is sent to the application. For more information, see 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol-monitormedia">ITLegacyCallMediaControl::MonitorMedia</a>.

## -parameters

### -param hCall

Handle to the call. The call state of <i>hCall</i> can be any state except idle.

### -param dwMediaModes

Media types to be monitored. If this parameter is zero, it cancels all media type detection. This parameter uses one or more of the 
<a href="/windows/desktop/Tapi/linemediamode--constants">LINEMEDIAMODE_ Constants</a>.

## -returns

Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_INVALMEDIAMODE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_UNINITIALIZED.

## -remarks

The media types specified with 
<a href="/windows/desktop/api/tapi/nf-tapi-lineopen">lineOpen</a> relate only to enabling the detection of these media types by the service provider for the purpose of handing off new incoming calls to the proper application. They do not impact any of the media-mode notification messages that are expected because of a previous invocation of 
<b>lineMonitorMedia</b>.

This function is considered successful if media type monitoring has been correctly initiated, not when media type monitoring has terminated. Media monitoring for a given media type remains in effect until it is explicitly disabled by calling 
<b>lineMonitorMedia</b> with a <i>dwMediaModes</i> parameter set to zero, until the call transitions to <i>idle</i>, or when the application deallocates its call handle for the call. The 
<b>lineMonitorMedia</b> function is primarily an event reporting mechanism. The media type (mode) of the call, as indicated in 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>, is not affected by the service provider's detection of the media type. Only the controlling application can change a call's media type.

Default media monitoring performed by the service provider corresponds to the union of all media types specified on 
<a href="/windows/desktop/api/tapi/nf-tapi-lineopen">lineOpen</a>.

Although this function can be invoked in any call state, a call's media type can typically only be detected while the call is in certain call states. These states can be device specific. For example, in ISDN, a message can indicate the media type of the media stream before the media stream exists. Similarly, distinctive ringing or the called identifier information about the call can be used to identify the media type of a call. Otherwise, the call may have to be answered (call in the <i>connected</i> state) to allow a service provider to determine the call's media type by filtering the media stream. Because filtering a call's media stream implies a computational overhead, applications should disable media monitoring when not required. By default, media monitoring is enabled for newly incoming calls, because a call's media type selects the application that should handle the call.

An outgoing application that deals with voice media types may want to monitor the call for silence (a tone) to distinguish who or what is at the called end of a call. For example, a person at home can answer calls with just a short "hello." A person in the office can provide a longer greeting, indicating name and company name. An answering machine can typically have an even longer greeting.

Because media-mode detection enabled by 
<b>lineMonitorMedia</b> is implemented as a read-only operation of the call's media stream, it is not disruptive.

Monitoring of media on a conference call applies only to the <i>hConfCall</i> parameter, not to the individual participating calls.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-lineopen">lineOpen</a>