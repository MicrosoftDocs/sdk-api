---
UID: NN:tapi3if.ITTAPI
title: ITTAPI (tapi3if.h)

description: The ITTAPI interface is the base interface for the TAPI object. The TAPI object is created by CoCreateInstance. For information on CoCreateInstance, see documentation on COM. All other TAPI 3 objects are created by TAPI 3 itself.
old-location: tapi3\ittapi.htm
tech.root: Tapi
ms.assetid: 75d641c7-dbf8-4ae2-b16b-2757e890d32b

ms.date: 12/05/2018
ms.keywords: ITTAPI, ITTAPI interface [TAPI 2.2], ITTAPI interface [TAPI 2.2],described, _tapi3_ittapi, tapi3.ittapi, tapi3if/ITTAPI
ms.topic: interface
f1_keywords: 
 - "tapi3if/ITTAPI"
dev_langs:
 - c++
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITTAPI
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITTAPI interface


## -description


The 
<b>ITTAPI</b> interface is the base interface for the TAPI object. The TAPI object is created by <b>CoCreateInstance</b>. For information on <b>CoCreateInstance</b>, see documentation on COM. All other TAPI 3 objects are created by TAPI 3 itself.

<b>ITTAPI</b> methods are provided to initialize a TAPI session, enumerate available addresses, register for CallHub and CallEvent notifications, and shut down a TAPI session.

The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2">ITTAPI2</a> interface derives from the 
<b>ITTAPI</b> interface. It adds additional methods on the TAPI object to support phone devices.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITTAPI</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITTAPI</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITTAPI</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses">EnumerateAddresses</a>
</td>
<td align="left" width="63%">
Enumerates addresses currently available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumeratecallhubs">EnumerateCallHubs</a>
</td>
<td align="left" width="63%">
Enumerates currently available call hubs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateprivatetapiobjects">EnumeratePrivateTAPIObjects</a>
</td>
<td align="left" width="63%">
Enumerates the currently available private objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses">get_Addresses</a>
</td>
<td align="left" width="63%">
Creates a collection of addresses currently available. Provided for Automation client applications, such as those written in Microsoft Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_callhubs">get_CallHubs</a>
</td>
<td align="left" width="63%">
Creates a collection of currently available call hubs. Provided for Automation client applications, such as those written in Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_eventfilter">get_EventFilter</a>
</td>
<td align="left" width="63%">
Get the current event filter mask.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_privatetapiobjects">get_PrivateTAPIObjects</a>
</td>
<td align="left" width="63%">
Creates a collection of currently existing TAPI private objects. Provided for Automation client applications, such as those written in Microsoft Visual Basic..

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes TAPI object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">put_EventFilter</a>
</td>
<td align="left" width="63%">
Sets the event filter mask. If no filter is set, no events are received.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications">RegisterCallNotifications</a>
</td>
<td align="left" width="63%">
Registers for call notification events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registerrequestrecipient">RegisterRequestRecipient</a>
</td>
<td align="left" width="63%">
Registers an application to handle assisted telephony requests.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-setapplicationpriority">SetApplicationPriority</a>
</td>
<td align="left" width="63%">
Sets priority under which applications will have calls passed to them by media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-setassistedtelephonypriority">SetAssistedTelephonyPriority</a>
</td>
<td align="left" width="63%">
Sets application priority to handle assisted telephony requests.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-setcallhubtracking">SetCallHubTracking</a>
</td>
<td align="left" width="63%">
Enables or disables CallHub tracking.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-shutdown">Shutdown</a>
</td>
<td align="left" width="63%">
Shuts down TAPI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-unregisternotifications">UnregisterNotifications</a>
</td>
<td align="left" width="63%">
Removes notifications for TAPI object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ittapi2">ITTAPI2</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapi-object">TAPI Object</a>
 

 

