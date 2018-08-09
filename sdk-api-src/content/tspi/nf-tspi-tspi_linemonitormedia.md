---
UID: NF:tspi.TSPI_lineMonitorMedia
title: TSPI_lineMonitorMedia function
author: windows-sdk-content
description: The TSPI_lineMonitorMedia function enables and disables the detection of media types on the specified call. When a media type is detected, a LINE_MONITORMEDIA message is sent to TAPI.
old-location: tspi\tspi_linemonitormedia.htm
old-project: tapi
ms.assetid: 56a7207a-0ddf-49e6-91f9-e47db6df3b61
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: TSPI_lineMonitorMedia, TSPI_lineMonitorMedia function [TAPI 2.2], _tspi_tspi_linemonitormedia, tspi.tspi_linemonitormedia, tspi/TSPI_lineMonitorMedia
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: AAAccountingData
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineMonitorMedia
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TSPI_lineMonitorMedia function


## -description


The 
<b>TSPI_lineMonitorMedia</b> function enables and disables the detection of media types on the specified call. When a media type is detected, a 
<a href="https://msdn.microsoft.com/0b285b3c-18a8-44a3-bba9-b53e247d16a1">LINE_MONITORMEDIA</a> message is sent to TAPI.


## -parameters




### -param hdCall

The handle to the call for which media monitoring is to be set. The call state of <i>hdCall</i> can be any state except <i>idle</i>.


### -param dwMediaModes

The media types to be monitored. The <i>dwMediaModes</i> parameter can have one of the 
<a href="https://msdn.microsoft.com/cbb758be-3ecd-4ac4-b1b5-57136a1aad8e">LINEMEDIAMODE_ constants</a>. 




A value of 0 cancels all media type monitoring.


## -returns



Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_INVALMEDIAMODE, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM.




## -remarks



The service provider returns LINEERR_INVALMEDIAMODE if the list of media types to be monitored contains invalid information.

This function returns zero (success) when media type monitoring has been correctly initiated, not when media type monitoring has terminated. Media monitoring for a given media type remains in effect until it is explicitly disabled by calling 
<b>TSPI_lineMonitorMedia</b> with a <i>dwMediaModes</i> parameter with the media type set to zero, or until the call transitions to <i>idle</i>.

<b>TSPI_lineMonitorMedia</b> is primarily an event reporting mechanism. The media type of a call, as indicated in 
<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a>, is not affected by the service provider's detection of the media type. Only TAPI or a client application can change a call's indicated media type using 
<a href="https://msdn.microsoft.com/3a0a5daf-eb4a-4e60-b343-8a47d342a86a">TSPI_lineSetMediaMode</a>. The actual use of a particular media type occurs through separate media stream APIs (such as Comm or WAVE).

Default media monitoring performed by the service provider for a new call appearance corresponds to the union of all media types specified by 
<a href="https://msdn.microsoft.com/407fa545-6890-4a8c-b5a8-bddeacc46e18">TSPI_lineSetDefaultMediaDetection</a>. Shortly after a new call is established, TAPI typically calls 
<b>TSPI_lineMonitorMedia</b> to reduce the set of media types detected and reported for this call to the union of all media types desired by the call's client applications.

The service provider must cancel media monitoring when a call goes idle. TAPI must compute the union of media types desired by all clients, and pass the result to this function. The service provider uses the set passed to this function by TAPI.

Although this function can be invoked in any call state, a call's media type can typically only be detected while the call is in certain call states. These states can be device specific. For example, in ISDN a message can indicate the media type of the media stream before the media stream exists. Similarly, distinctive ringing or the called ID information about the call can be used to identify the media type of a call. Otherwise, the call may have to be answered (call in the <i>connected</i> state) to allow a service provider to determine the call's media type by filtering of the media stream. Because filtering of a call's media stream implies a computational overhead, TAPI typically uses this procedure to disable media monitoring when it is not required.

Because media-mode detection enabled by 
<b>TSPI_lineMonitorMedia</b> is implemented as a read-only operation of the call's media stream, it is not disruptive. No signals are sent on the line as a result of setting 
<b>TSPI_lineMonitorMedia</b>.

Regarding the passed media type, TAPI guarantees that there are no reserved bits set. The service provider must perform any further validity checks on the media types, such as checking whether any media types are indeed supported by the service provider.




## -see-also




<a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a>



<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>



<a href="https://msdn.microsoft.com/cbb758be-3ecd-4ac4-b1b5-57136a1aad8e">LINEMEDIAMODE_ Constants</a>



<a href="https://msdn.microsoft.com/0b285b3c-18a8-44a3-bba9-b53e247d16a1">LINE_MONITORMEDIA</a>



<a href="https://msdn.microsoft.com/8fa3f9ab-1749-43c8-b2a5-c481b1f94177">TSPI_lineConditionalMediaDetection</a>



<a href="https://msdn.microsoft.com/6c5a668e-9a9a-4a7a-98e9-bd8ec4b819b2">TSPI_lineGetDevCaps</a>



<a href="https://msdn.microsoft.com/407fa545-6890-4a8c-b5a8-bddeacc46e18">TSPI_lineSetDefaultMediaDetection</a>



<a href="https://msdn.microsoft.com/e9273bd6-8dc3-4b45-bf0e-a1a10d78a604">TSPI_lineSetMediaControl</a>



<a href="https://msdn.microsoft.com/3a0a5daf-eb4a-4e60-b343-8a47d342a86a">TSPI_lineSetMediaMode</a>
 

 

