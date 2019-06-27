---
UID: NN:tapi3if.ITBasicCallControl
title: ITBasicCallControl (tapi3if.h)
author: windows-sdk-content
description: The ITBasicCallControl interface is used by the application to connect, answer, and perform basic telephony operations on a call object.
old-location: tapi3\itbasiccallcontrol.htm
tech.root: Tapi
ms.assetid: a0b4c496-5ee8-4810-8170-8ea505c99f18
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITBasicCallControl, ITBasicCallControl interface [TAPI 2.2], ITBasicCallControl interface [TAPI 2.2],described, _tapi3_itbasiccallcontrol, tapi3.itbasiccallcontrol, tapi3if/ITBasicCallControl
ms.topic: interface
f1_keywords: 
 - "tapi3if/ITBasicCallControl"
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
 - ITBasicCallControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITBasicCallControl interface


## -description


The 
<b>ITBasicCallControl</b> interface is used by the application to connect, answer, and perform basic telephony operations on a 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/call-object">call object</a>.

The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2">ITBasicCallControl2</a> interface is an extension of the 
<b>ITBasicCallControl</b> interface. 
<b>ITBasicCallControl2</b> supplies additional methods that allow an application to select a terminal onto a call. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall">ITAddress::CreateCall</a> method creates the 
<b>ITBasicCallControl</b> interface.

Note to programmers familiar with TAPI 2.1: The general function of this interface is similar to the TAPI 2.1 line functions. For example, the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi/nf-tapi-lineanswer">lineAnswer</a> function and the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer">ITBasicCallControl::Answer</a> method provide similar functionality.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITBasicCallControl</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITBasicCallControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITBasicCallControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer">Answer</a>
</td>
<td align="left" width="63%">
Answers an incoming call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-blindtransfer">BlindTransfer</a>
</td>
<td align="left" width="63%">
Transfers the call to the indicated address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-conference">Conference</a>
</td>
<td align="left" width="63%">
Starts a conference, with the current call included.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect">Connect</a>
</td>
<td align="left" width="63%">
Attempts to complete the connection of an outgoing call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-dial">Dial</a>
</td>
<td align="left" width="63%">
Dials the given address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects the call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish">Finish</a>
</td>
<td align="left" width="63%">
Finishes the two-step process of transferring or adding the call to a conference.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-handoffdirect">HandoffDirect</a>
</td>
<td align="left" width="63%">
Hands off the call to a specific application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-handoffindirect">HandoffIndirect</a>
</td>
<td align="left" width="63%">
Hands off the call to another application, specifying only the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapimediatype--constants">media type</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-hold">Hold</a>
</td>
<td align="left" width="63%">
Places or removes the call from the hold state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkdirect">ParkDirect</a>
</td>
<td align="left" width="63%">
Parks the call at a specified address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkindirect">ParkIndirect</a>
</td>
<td align="left" width="63%">
Parks the call and returns the parked address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-pickup">Pickup</a>
</td>
<td align="left" width="63%">
Picks up a call alerting at the specified group identification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-removefromconference">RemoveFromConference</a>
</td>
<td align="left" width="63%">
Removes the call from a conference.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos">SetQOS</a>
</td>
<td align="left" width="63%">
Sets the QOS service level for the call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-swaphold">SwapHold</a>
</td>
<td align="left" width="63%">
Swaps the call (which is active) with the specified call on hold.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-transfer">Transfer</a>
</td>
<td align="left" width="63%">
Transfers the current call to the destination address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-unpark">Unpark</a>
</td>
<td align="left" width="63%">
Gets the call parked at the specified address.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/call-object">Call Object</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2">ITBasicCallControl2</a>
 

 

