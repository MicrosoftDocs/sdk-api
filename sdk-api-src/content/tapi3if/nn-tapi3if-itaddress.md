---
UID: NN:tapi3if.ITAddress
title: ITAddress (tapi3if.h)

description: The ITAddress interface is the base interface for the Address object. Applications use this interface to get information about and use the Address object.
old-location: tapi3\itaddress.htm
tech.root: Tapi
ms.assetid: 93f2e4cf-013e-4064-88d5-69fddd458274

ms.date: 12/05/2018
ms.keywords: ITAddress, ITAddress interface [TAPI 2.2], ITAddress interface [TAPI 2.2],described, _tapi3_itaddress, tapi3.itaddress, tapi3if/ITAddress
ms.topic: interface
f1_keywords: 
 - "tapi3if/ITAddress"
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
 - ITAddress
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAddress interface


## -description


The 
<b>ITAddress</b> interface is the base interface for the Address object. Applications use this interface to get information about and use the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/address-object">Address object</a>.

The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddress2">ITAddress2</a> interface derives from the 
<b>ITAddress</b> interface. 
<b>ITAddress2</b> adds methods to the Address object in order to support phone devices. The 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumaddress-next">IEnumAddress::Next</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses">ITTapi::get_Addresses</a> methods create the 
<b>ITAddress</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAddress</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITAddress</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall">CreateCall</a>
</td>
<td align="left" width="63%">
Creates a new Call object that can be used to make an outgoing call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createforwardinfoobject">CreateForwardInfoObject</a>
</td>
<td align="left" width="63%">
Creates 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation">ITForwardInformation</a>, the forwarding information object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-enumeratecalls">EnumerateCalls</a>
</td>
<td align="left" width="63%">
Enumerates calls on the current address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward">Forward</a>
</td>
<td align="left" width="63%">
Forwards calls destined for the address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_addressname">get_AddressName</a>
</td>
<td align="left" width="63%">
Gets the name of the address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_calls">get_Calls</a>
</td>
<td align="left" width="63%">
Creates a collection of calls on the current address. Provided for Automation client applications, such as those written in Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo">get_CurrentForwardInfo</a>
</td>
<td align="left" width="63%">
Gets a pointer to the forwarding information object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_dialableaddress">get_DialableAddress</a>
</td>
<td align="left" width="63%">
Gets the <b>BSTR</b> which can be used to connect to this address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_donotdisturb">get_DoNotDisturb</a>
</td>
<td align="left" width="63%">
Gets the current status of the do not disturb feature on the address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_messagewaiting">get_MessageWaiting</a>
</td>
<td align="left" width="63%">
Determines if the address has a message waiting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_serviceprovidername">get_ServiceProviderName</a>
</td>
<td align="left" width="63%">
Gets the service provider name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_state">get_State</a>
</td>
<td align="left" width="63%">
Gets the current state of the address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_tapiobject">get_TAPIObject</a>
</td>
<td align="left" width="63%">
Gets pointer to the TAPI object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-put_donotdisturb">put_DoNotDisturb</a>
</td>
<td align="left" width="63%">
Sets the do not disturb status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-put_messagewaiting">put_MessageWaiting</a>
</td>
<td align="left" width="63%">
Sets the status of the message waiting on the address.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/address-object">Address Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddress2">ITAddress2</a>
 

 

