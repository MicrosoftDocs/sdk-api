---
UID: NN:tapi3if.ITForwardInformation2
title: ITForwardInformation2 (tapi3if.h)
author: windows-sdk-content
description: The ITForwardInformation2 interface exposes methods that provide additional methods for the control of forwarding information. See ITForwardInformation for the basic forwarding control methods.
old-location: tapi3\itforwardinformation2.htm
tech.root: Tapi
ms.assetid: 25c99955-1a9d-49fa-9432-962e19296ad5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITForwardInformation2, ITForwardInformation2 interface [TAPI 2.2], ITForwardInformation2 interface [TAPI 2.2],described, _tapi3_itforwardinformation2, tapi3.itforwardinformation2, tapi3if/ITForwardInformation2
ms.topic: interface
f1_keywords: 
 - "tapi3if/ITForwardInformation2"
req.header: tapi3if.h
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
 - ITForwardInformation2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITForwardInformation2 interface


## -description


The 
<b>ITForwardInformation2</b> interface exposes methods that provide additional methods for the control of forwarding information. See 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation">ITForwardInformation</a> for the basic forwarding control methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITForwardInformation2</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITForwardInformation2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITForwardInformation2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itforwardinformation2-get_forwardtypecalleraddresstype">get_ForwardTypeCallerAddressType</a>
</td>
<td align="left" width="63%">
Gets the destination address type for a given forwarding type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itforwardinformation2-get_forwardtypedestinationaddresstype">get_ForwardTypeDestinationAddressType</a>
</td>
<td align="left" width="63%">
Gets the caller address type for a given forwarding type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itforwardinformation2-getforwardtype2">GetForwardType2</a>
</td>
<td align="left" width="63%">
Gets the current forwarding mode, specified by caller address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itforwardinformation2-setforwardtype2">SetForwardType2</a>
</td>
<td align="left" width="63%">
Sets the current forwarding mode, specified by caller address.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createforwardinfoobject">ITAddress::CreateForwardInfoObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward">ITAddress::Forward</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo">ITAddress::get_CurrentForwardInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation">ITForwardInformation</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/terminal-object">Terminal Object</a>
 

 

