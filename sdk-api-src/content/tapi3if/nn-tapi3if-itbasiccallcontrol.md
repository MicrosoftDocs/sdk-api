---
UID: NN:tapi3if.ITBasicCallControl
title: ITBasicCallControl
author: windows-sdk-content
description: The ITBasicCallControl interface is used by the application to connect, answer, and perform basic telephony operations on a call object.
old-location: tapi3\itbasiccallcontrol.htm
old-project: tapi
ms.assetid: a0b4c496-5ee8-4810-8170-8ea505c99f18
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITBasicCallControl, ITBasicCallControl interface [TAPI 2.2], ITBasicCallControl interface [TAPI 2.2],described, _tapi3_itbasiccallcontrol, tapi3.itbasiccallcontrol, tapi3if/ITBasicCallControl
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TERMINAL_TYPE
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITBasicCallControl interface


## -description


The 
<b>ITBasicCallControl</b> interface is used by the application to connect, answer, and perform basic telephony operations on a 
<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">call object</a>.

The 
<a href="https://msdn.microsoft.com/fc693221-b7ba-4b33-aed7-59ec92fc9b58">ITBasicCallControl2</a> interface is an extension of the 
<b>ITBasicCallControl</b> interface. 
<b>ITBasicCallControl2</b> supplies additional methods that allow an application to select a terminal onto a call. The 
<a href="https://msdn.microsoft.com/1b5a755c-fdaf-42ca-9747-9b34efbd0ac3">ITAddress::CreateCall</a> method creates the 
<b>ITBasicCallControl</b> interface.

Note to programmers familiar with TAPI 2.1: The general function of this interface is similar to the TAPI 2.1 line functions. For example, the 
<a href="https://msdn.microsoft.com/dd51991c-c044-4b88-8f97-9e0ae701a2a5">lineAnswer</a> function and the 
<a href="https://msdn.microsoft.com/81928cf7-082e-44e1-a631-a50a1f01ecec">ITBasicCallControl::Answer</a> method provide similar functionality.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITBasicCallControl</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITBasicCallControl</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541235">Answer</a>
</td>
<td align="left" width="63%">
Answers an incoming call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/766a48af-512a-4ad6-99e1-436141bf8447">BlindTransfer</a>
</td>
<td align="left" width="63%">
Transfers the call to the indicated address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73721921-c943-4adc-a2b1-e8c19ec809ac">Conference</a>
</td>
<td align="left" width="63%">
Starts a conference, with the current call included.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc9a8bfd-14c0-459c-a911-325b73323c08">Connect</a>
</td>
<td align="left" width="63%">
Attempts to complete the connection of an outgoing call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31fea4d8-9028-48d5-9f5d-53f1451103c7">Dial</a>
</td>
<td align="left" width="63%">
Dials the given address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7d556fd-d3f5-4b93-96a9-cc5c58fb8a95">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects the call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b0bd871-b618-4c24-a717-62a248112d97">Finish</a>
</td>
<td align="left" width="63%">
Finishes the two-step process of transferring or adding the call to a conference.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a96a3790-ee5d-4983-b69a-30c7af96afd9">HandoffDirect</a>
</td>
<td align="left" width="63%">
Hands off the call to a specific application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02579638-fafd-4c4a-91a3-460d7ebf6917">HandoffIndirect</a>
</td>
<td align="left" width="63%">
Hands off the call to another application, specifying only the 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media type</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44f1d3fd-6c48-41f4-a30e-83bf2ce19fde">Hold</a>
</td>
<td align="left" width="63%">
Places or removes the call from the hold state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6461fd21-1726-4d24-8a17-d687b807b8e3">ParkDirect</a>
</td>
<td align="left" width="63%">
Parks the call at a specified address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/661ad11c-b653-4b70-9553-59d484527c29">ParkIndirect</a>
</td>
<td align="left" width="63%">
Parks the call and returns the parked address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25da3cf2-50f0-4f64-94ce-cf952e057376">Pickup</a>
</td>
<td align="left" width="63%">
Picks up a call alerting at the specified group identification.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3a357a1-9bfa-4d23-b7d7-e1d9b636e861">RemoveFromConference</a>
</td>
<td align="left" width="63%">
Removes the call from a conference.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1e6ef32-5706-4b1c-a1fa-a7be48fd6efd">SetQOS</a>
</td>
<td align="left" width="63%">
Sets the QOS service level for the call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/372e8ca9-53fb-4ec0-aae8-52f85523b7c4">SwapHold</a>
</td>
<td align="left" width="63%">
Swaps the call (which is active) with the specified call on hold.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f2a06e6-9f0b-4bf3-9f18-6e9f57c4b02f">Transfer</a>
</td>
<td align="left" width="63%">
Transfers the current call to the destination address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4cea44e-0dac-4021-a42c-b136c2e686e0">Unpark</a>
</td>
<td align="left" width="63%">
Gets the call parked at the specified address.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/fc693221-b7ba-4b33-aed7-59ec92fc9b58">ITBasicCallControl2</a>
 

 

