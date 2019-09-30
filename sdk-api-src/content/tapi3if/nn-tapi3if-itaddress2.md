---
UID: NN:tapi3if.ITAddress2
title: ITAddress2 (tapi3if.h)
author: windows-sdk-content
description: The ITAddress2 interface derives from the ITAddress interface. ITAddress2 adds methods to the Address object in order to support phone devices. All Address objects enumerated from TAPI 3.1 automatically implement this interface.
old-location: tapi3\itaddress2.htm
tech.root: Tapi
ms.assetid: 3cc47291-8130-45bd-8db8-c5d1b463507d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITAddress2, ITAddress2 interface [TAPI 2.2], ITAddress2 interface [TAPI 2.2],described, _tapi3_itaddress2, tapi3.itaddress2, tapi3if/ITAddress2
ms.topic: interface
f1_keywords: 
 - "tapi3if/ITAddress2"
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
 - ITAddress2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAddress2 interface


## -description


The 
<b>ITAddress2</b> interface derives from the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface. 
<b>ITAddress2</b> adds methods to the Address object in order to support phone devices. All Address objects enumerated from TAPI 3.1 automatically implement this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAddress2</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITAddress2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITAddress2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress2-devicespecific">DeviceSpecific</a>
</td>
<td align="left" width="63%">
Provides access to device-specific features. This method is intended for C/C++ applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress2-devicespecificvariant">DeviceSpecificVariant</a>
</td>
<td align="left" width="63%">
Provides access to device-specific features. This method is intended for Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress2-enumeratephones">EnumeratePhones</a>
</td>
<td align="left" width="63%">
Enumerates the phone objects corresponding to the phone devices that can be used with this address. This method is intended for C/C++ applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress2-enumeratepreferredphones">EnumeratePreferredPhones</a>
</td>
<td align="left" width="63%">
Enumerates the phone objects corresponding to the phone devices that are preferred for use with this address. This method is intended for C/C++ applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress2-get_eventfilter">get_EventFilter</a>
</td>
<td align="left" width="63%">
Gets event filters for this address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress2-get_phones">get_Phones</a>
</td>
<td align="left" width="63%">
Gets a collection of phone objects that can be used with this address. This method is intended for Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress2-get_preferredphones">get_PreferredPhones</a>
</td>
<td align="left" width="63%">
Returns a collection of phone objects corresponding to the phone devices that are preferred for use with this address. This method is intended for Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress2-getphonefromterminal">GetPhoneFromTerminal</a>
</td>
<td align="left" width="63%">
Gets the phone object associated with the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress2-negotiateextversion">NegotiateExtVersion</a>
</td>
<td align="left" width="63%">
Negotiates an extension version to use with the specified line device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddress2-put_eventfilter">put_EventFilter</a>
</td>
<td align="left" width="63%">
Sets event filters for this address.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>
 

 

