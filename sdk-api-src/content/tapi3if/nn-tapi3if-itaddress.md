---
UID: NN:tapi3if.ITAddress
title: ITAddress
author: windows-sdk-content
description: The ITAddress interface is the base interface for the Address object. Applications use this interface to get information about and use the Address object.
old-location: tapi3\itaddress.htm
tech.root: tapi
ms.assetid: 93f2e4cf-013e-4064-88d5-69fddd458274
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ITAddress, ITAddress interface [TAPI 2.2], ITAddress interface [TAPI 2.2],described, _tapi3_itaddress, tapi3.itaddress, tapi3if/ITAddress
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
 - ITAddress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAddress interface


## -description


The 
<b>ITAddress</b> interface is the base interface for the Address object. Applications use this interface to get information about and use the 
<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address object</a>.

The 
<a href="https://msdn.microsoft.com/3cc47291-8130-45bd-8db8-c5d1b463507d">ITAddress2</a> interface derives from the 
<b>ITAddress</b> interface. 
<b>ITAddress2</b> adds methods to the Address object in order to support phone devices. The 
<a href="https://msdn.microsoft.com/14bc32c4-8b59-41ec-a7f6-1ed7f26ae62a">IEnumAddress::Next</a> and 
<a href="https://msdn.microsoft.com/9e70ae94-20a2-4ba4-ab39-794f611011d8">ITTapi::get_Addresses</a> methods create the 
<b>ITAddress</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAddress</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITAddress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITAddress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b5a755c-fdaf-42ca-9747-9b34efbd0ac3">CreateCall</a>
</td>
<td align="left" width="63%">
Creates a new Call object that can be used to make an outgoing call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87d37ba3-5398-47a7-808b-eb9b6681653d">CreateForwardInfoObject</a>
</td>
<td align="left" width="63%">
Creates 
<a href="https://msdn.microsoft.com/0e06cd0b-b95b-4853-b883-53146be084f0">ITForwardInformation</a>, the forwarding information object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ffa90bf-3005-4fd0-b52f-b155c8b2194f">EnumerateCalls</a>
</td>
<td align="left" width="63%">
Enumerates calls on the current address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f070b50-db9a-49e8-a0f3-e448c5dee144">Forward</a>
</td>
<td align="left" width="63%">
Forwards calls destined for the address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb26dcf5-0192-4156-914b-9aa6e76a2bd2">get_AddressName</a>
</td>
<td align="left" width="63%">
Gets the name of the address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0b16578-0530-4ff9-a7ce-d36527ed2da9">get_Calls</a>
</td>
<td align="left" width="63%">
Creates a collection of calls on the current address. Provided for Automation client applications, such as those written in Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7817ac03-d9fc-4042-ae7d-350ee6cbef53">get_CurrentForwardInfo</a>
</td>
<td align="left" width="63%">
Gets a pointer to the forwarding information object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d6dcbbe-3372-4346-8f5e-fb34b7aca88d">get_DialableAddress</a>
</td>
<td align="left" width="63%">
Gets the <b>BSTR</b> which can be used to connect to this address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9257201-bcd1-4d6b-9bc7-24b323cd4f15">get_DoNotDisturb</a>
</td>
<td align="left" width="63%">
Gets the current status of the do not disturb feature on the address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ddb49d9-dde7-498b-a243-f8c5b1294a87">get_MessageWaiting</a>
</td>
<td align="left" width="63%">
Determines if the address has a message waiting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa49d256-58e0-4d7e-a121-387a3a704519">get_ServiceProviderName</a>
</td>
<td align="left" width="63%">
Gets the service provider name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f68d0fb0-126d-4464-9d5a-0ffae4d40cb7">get_State</a>
</td>
<td align="left" width="63%">
Gets the current state of the address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37064bef-d5c0-44b9-a7eb-ae922b175f91">get_TAPIObject</a>
</td>
<td align="left" width="63%">
Gets pointer to the TAPI object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d3071d5-055a-469d-aa17-984b8210cbea">put_DoNotDisturb</a>
</td>
<td align="left" width="63%">
Sets the do not disturb status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9dc125ab-a452-4108-93d5-9f341b879e8d">put_MessageWaiting</a>
</td>
<td align="left" width="63%">
Sets the status of the message waiting on the address.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/3cc47291-8130-45bd-8db8-c5d1b463507d">ITAddress2</a>
 

 

