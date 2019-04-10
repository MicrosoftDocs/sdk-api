---
UID: NN:tapi3if.ITTAPI
title: ITTAPI (tapi3if.h)
author: windows-sdk-content
description: The ITTAPI interface is the base interface for the TAPI object. The TAPI object is created by CoCreateInstance. For information on CoCreateInstance, see documentation on COM. All other TAPI 3 objects are created by TAPI 3 itself.
old-location: tapi3\ittapi.htm
tech.root: Tapi
ms.assetid: 75d641c7-dbf8-4ae2-b16b-2757e890d32b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITTAPI, ITTAPI interface [TAPI 2.2], ITTAPI interface [TAPI 2.2],described, _tapi3_ittapi, tapi3.ittapi, tapi3if/ITTAPI
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTAPI interface


## -description


The 
<b>ITTAPI</b> interface is the base interface for the TAPI object. The TAPI object is created by <b>CoCreateInstance</b>. For information on <b>CoCreateInstance</b>, see documentation on COM. All other TAPI 3 objects are created by TAPI 3 itself.

<b>ITTAPI</b> methods are provided to initialize a TAPI session, enumerate available addresses, register for CallHub and CallEvent notifications, and shut down a TAPI session.

The 
<a href="https://msdn.microsoft.com/8c67f31e-783e-4371-9f17-063f8ecfc069">ITTAPI2</a> interface derives from the 
<b>ITTAPI</b> interface. It adds additional methods on the TAPI object to support phone devices.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITTAPI</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITTAPI</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b40a2071-24bf-470c-bfba-de23317e8652">EnumerateAddresses</a>
</td>
<td align="left" width="63%">
Enumerates addresses currently available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98d20aa3-6d4c-4971-aa4a-5b9632038eb1">EnumerateCallHubs</a>
</td>
<td align="left" width="63%">
Enumerates currently available call hubs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/071166d9-99ff-4245-b4c8-0b89b8bae19c">EnumeratePrivateTAPIObjects</a>
</td>
<td align="left" width="63%">
Enumerates the currently available private objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e70ae94-20a2-4ba4-ab39-794f611011d8">get_Addresses</a>
</td>
<td align="left" width="63%">
Creates a collection of addresses currently available. Provided for Automation client applications, such as those written in Microsoft Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57177526-1351-4f59-8f24-74d8b87d27c0">get_CallHubs</a>
</td>
<td align="left" width="63%">
Creates a collection of currently available call hubs. Provided for Automation client applications, such as those written in Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0544e9f-0bfc-43ab-bcf0-800afb0ebfcf">get_EventFilter</a>
</td>
<td align="left" width="63%">
Get the current event filter mask.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a196e6cc-d8a3-49a2-8bda-e99675806dd7">get_PrivateTAPIObjects</a>
</td>
<td align="left" width="63%">
Creates a collection of currently existing TAPI private objects. Provided for Automation client applications, such as those written in Microsoft Visual Basic..

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/822ca3fe-8deb-4fe3-8b83-060eae69840c">Initialize</a>
</td>
<td align="left" width="63%">
Initializes TAPI object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/126ec551-aade-47d8-987f-1f735f10bd28">put_EventFilter</a>
</td>
<td align="left" width="63%">
Sets the event filter mask. If no filter is set, no events are received.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/335deb2c-7700-4101-b6fa-f7fe0f248307">RegisterCallNotifications</a>
</td>
<td align="left" width="63%">
Registers for call notification events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bee5348e-99f0-4168-9021-112fc16d8921">RegisterRequestRecipient</a>
</td>
<td align="left" width="63%">
Registers an application to handle assisted telephony requests.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca049695-02d0-4b30-ad1f-60cdbf0a4dbd">SetApplicationPriority</a>
</td>
<td align="left" width="63%">
Sets priority under which applications will have calls passed to them by media.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/446fd541-30af-45de-85fa-d6655317362c">SetAssistedTelephonyPriority</a>
</td>
<td align="left" width="63%">
Sets application priority to handle assisted telephony requests.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c33a294-ed45-4353-91ed-fa0d3d66e5da">SetCallHubTracking</a>
</td>
<td align="left" width="63%">
Enables or disables CallHub tracking.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64abb427-d41a-4670-a01c-095c678de6ff">Shutdown</a>
</td>
<td align="left" width="63%">
Shuts down TAPI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66717165-1c29-4d77-b6ac-8c3638fb11f4">UnregisterNotifications</a>
</td>
<td align="left" width="63%">
Removes notifications for TAPI object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/8c67f31e-783e-4371-9f17-063f8ecfc069">ITTAPI2</a>



<a href="https://msdn.microsoft.com/c4cf358f-2dc8-432a-92ed-68282ddc8a97">TAPI Object</a>
 

 

