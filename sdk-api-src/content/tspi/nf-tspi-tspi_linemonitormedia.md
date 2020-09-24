---
UID: NF:tspi.TSPI_lineMonitorMedia
title: TSPI_lineMonitorMedia function (tspi.h)
description: The TSPI_lineMonitorMedia function enables and disables the detection of media types on the specified call. When a media type is detected, a LINE_MONITORMEDIA message is sent to TAPI.
helpviewer_keywords: ["TSPI_lineMonitorMedia","TSPI_lineMonitorMedia function [TAPI 2.2]","_tspi_tspi_linemonitormedia","tspi.tspi_linemonitormedia","tspi/TSPI_lineMonitorMedia"]
old-location: tspi\tspi_linemonitormedia.htm
tech.root: tapi3
ms.assetid: 56a7207a-0ddf-49e6-91f9-e47db6df3b61
ms.date: 12/05/2018
ms.keywords: TSPI_lineMonitorMedia, TSPI_lineMonitorMedia function [TAPI 2.2], _tspi_tspi_linemonitormedia, tspi.tspi_linemonitormedia, tspi/TSPI_lineMonitorMedia
req.header: tspi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TSPI_lineMonitorMedia
 - tspi/TSPI_lineMonitorMedia
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineMonitorMedia
---

# TSPI_lineMonitorMedia function


## -description

The 
<b>TSPI_lineMonitorMedia</b> function enables and disables the detection of media types on the specified call. When a media type is detected, a 
<a href="/previous-versions/windows/desktop/legacy/ms725233(v=vs.85)">LINE_MONITORMEDIA</a> message is sent to TAPI.

## -parameters

### -param hdCall

The handle to the call for which media monitoring is to be set. The call state of <i>hdCall</i> can be any state except <i>idle</i>.

### -param dwMediaModes

The media types to be monitored. The <i>dwMediaModes</i> parameter can have one of the 
<a href="/windows/desktop/Tapi/linemediamode--constants">LINEMEDIAMODE_ constants</a>. 




A value of 0 cancels all media type monitoring.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_INVALMEDIAMODE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM.

## -remarks

The service provider returns LINEERR_INVALMEDIAMODE if the list of media types to be monitored contains invalid information.

This function returns zero (success) when media type monitoring has been correctly initiated, not when media type monitoring has terminated. Media monitoring for a given media type remains in effect until it is explicitly disabled by calling 
<b>TSPI_lineMonitorMedia</b> with a <i>dwMediaModes</i> parameter with the media type set to zero, or until the call transitions to <i>idle</i>.

<b>TSPI_lineMonitorMedia</b> is primarily an event reporting mechanism. The media type of a call, as indicated in 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>, is not affected by the service provider's detection of the media type. Only TAPI or a client application can change a call's indicated media type using 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetmediamode">TSPI_lineSetMediaMode</a>. The actual use of a particular media type occurs through separate media stream APIs (such as Comm or WAVE).

Default media monitoring performed by the service provider for a new call appearance corresponds to the union of all media types specified by 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection">TSPI_lineSetDefaultMediaDetection</a>. Shortly after a new call is established, TAPI typically calls 
<b>TSPI_lineMonitorMedia</b> to reduce the set of media types detected and reported for this call to the union of all media types desired by the call's client applications.

The service provider must cancel media monitoring when a call goes idle. TAPI must compute the union of media types desired by all clients, and pass the result to this function. The service provider uses the set passed to this function by TAPI.

Although this function can be invoked in any call state, a call's media type can typically only be detected while the call is in certain call states. These states can be device specific. For example, in ISDN a message can indicate the media type of the media stream before the media stream exists. Similarly, distinctive ringing or the called ID information about the call can be used to identify the media type of a call. Otherwise, the call may have to be answered (call in the <i>connected</i> state) to allow a service provider to determine the call's media type by filtering of the media stream. Because filtering of a call's media stream implies a computational overhead, TAPI typically uses this procedure to disable media monitoring when it is not required.

Because media-mode detection enabled by 
<b>TSPI_lineMonitorMedia</b> is implemented as a read-only operation of the call's media stream, it is not disruptive. No signals are sent on the line as a result of setting 
<b>TSPI_lineMonitorMedia</b>.

Regarding the passed media type, TAPI guarantees that there are no reserved bits set. The service provider must perform any further validity checks on the media types, such as checking whether any media types are indeed supported by the service provider.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/windows/desktop/Tapi/linemediamode--constants">LINEMEDIAMODE_ Constants</a>



<a href="/previous-versions/windows/desktop/legacy/ms725233(v=vs.85)">LINE_MONITORMEDIA</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_lineconditionalmediadetection">TSPI_lineConditionalMediaDetection</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetdevcaps">TSPI_lineGetDevCaps</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection">TSPI_lineSetDefaultMediaDetection</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetmediacontrol">TSPI_lineSetMediaControl</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetmediamode">TSPI_lineSetMediaMode</a>