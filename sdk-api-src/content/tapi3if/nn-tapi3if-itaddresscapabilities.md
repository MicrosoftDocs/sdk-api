---
UID: NN:tapi3if.ITAddressCapabilities
title: ITAddressCapabilities (tapi3if.h)
description: The ITAddressCapabilities interface is used to obtain information about an address's capabilities. It is on the Address object, and an application can access it by calling QueryInterface on the Address object.
old-location: tapi3\itaddresscapabilities.htm
tech.root: Tapi
ms.assetid: 36f452ce-9171-41da-b003-4c7df17790da
ms.date: 12/05/2018
ms.keywords: ITAddressCapabilities, ITAddressCapabilities interface [TAPI 2.2], ITAddressCapabilities interface [TAPI 2.2],described, _tapi3_itaddresscapabilities, tapi3.itaddresscapabilities, tapi3if/ITAddressCapabilities
ms.topic: interface
f1_keywords:
- tapi3if/ITAddressCapabilities
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
- ITAddressCapabilities
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAddressCapabilities interface


## -description


The 
<b>ITAddressCapabilities</b> interface is used to obtain information about an address's capabilities. It is on the Address object, and an application can access it by calling <b>QueryInterface</b> on the Address object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAddressCapabilities</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITAddressCapabilities</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITAddressCapabilities</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-enumeratecalltreatments">EnumerateCallTreatments</a>
</td>
<td align="left" width="63%">
Gets call treatments. This method is provided for applications written in C/C++ and Java.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-enumeratecompletionmessages">EnumerateCompletionMessages</a>
</td>
<td align="left" width="63%">
Gets completion messages. This method is provided for applications written in C/C++ and Java.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-enumeratedeviceclasses">EnumerateDeviceClasses</a>
</td>
<td align="left" width="63%">
Gets device classes. This method is provided for applications written in C/C++ and Java.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability">get_AddressCapability</a>
</td>
<td align="left" width="63%">
Gets the capability value for a given 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-address_capability">ADDRESS_CAPABILITY</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapabilitystring">get_AddressCapabilityString</a>
</td>
<td align="left" width="63%">
Gets the capability string for a given 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-address_capability_string">ADDRESS_CAPABILITY_STRING</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_calltreatments">get_CallTreatments</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/linecalltreatment--constants">call treatment</a>. This method is provided for Automation client applications, such as those written in Visual Basic and scripting languages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_completionmessages">get_CompletionMessages</a>
</td>
<td align="left" width="63%">
Gets completion messages. This method is provided for Automation client applications, such as those written in Visual Basic and scripting languages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_deviceclasses">get_DeviceClasses</a>
</td>
<td align="left" width="63%">
Gets 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapi-device-classes">device classes</a>. This method is provided for Automation client applications, such as those written in Visual Basic and scripting languages.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/address-object">Address Object</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

