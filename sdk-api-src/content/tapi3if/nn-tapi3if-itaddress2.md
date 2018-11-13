---
UID: NN:tapi3if.ITAddress2
title: ITAddress2
author: windows-sdk-content
description: The ITAddress2 interface derives from the ITAddress interface. ITAddress2 adds methods to the Address object in order to support phone devices. All Address objects enumerated from TAPI 3.1 automatically implement this interface.
old-location: tapi3\itaddress2.htm
tech.root: tapi
ms.assetid: 3cc47291-8130-45bd-8db8-c5d1b463507d
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITAddress2, ITAddress2 interface [TAPI 2.2], ITAddress2 interface [TAPI 2.2],described, _tapi3_itaddress2, tapi3.itaddress2, tapi3if/ITAddress2
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
 - ITAddress2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAddress2 interface


## -description


The 
<b>ITAddress2</b> interface derives from the 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a> interface. 
<b>ITAddress2</b> adds methods to the Address object in order to support phone devices. All Address objects enumerated from TAPI 3.1 automatically implement this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAddress2</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITAddress2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d3b9e04d-ec20-4e30-847f-eb77f426f0f3">DeviceSpecific</a>
</td>
<td align="left" width="63%">
Provides access to device-specific features. This method is intended for C/C++ applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27882bb2-dab8-4b8c-acca-35fbdc526362">DeviceSpecificVariant</a>
</td>
<td align="left" width="63%">
Provides access to device-specific features. This method is intended for Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/674a9c35-8949-4935-9fa2-800fced6b57b">EnumeratePhones</a>
</td>
<td align="left" width="63%">
Enumerates the phone objects corresponding to the phone devices that can be used with this address. This method is intended for C/C++ applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5a02f79-59b3-43f0-9b3b-fdd7839ba026">EnumeratePreferredPhones</a>
</td>
<td align="left" width="63%">
Enumerates the phone objects corresponding to the phone devices that are preferred for use with this address. This method is intended for C/C++ applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb0fbfc1-56bf-4455-8d6a-71c78b6a6534">get_EventFilter</a>
</td>
<td align="left" width="63%">
Gets event filters for this address.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5cd82f34-1f3f-46a2-bad3-954dc5b93d87">get_Phones</a>
</td>
<td align="left" width="63%">
Gets a collection of phone objects that can be used with this address. This method is intended for Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6cb17c83-86db-4d44-bbd3-80a0e52fec73">get_PreferredPhones</a>
</td>
<td align="left" width="63%">
Returns a collection of phone objects corresponding to the phone devices that are preferred for use with this address. This method is intended for Visual Basic and scripting applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d3873ad-ce3d-4b4c-907f-9c0dbf0ef206">GetPhoneFromTerminal</a>
</td>
<td align="left" width="63%">
Gets the phone object associated with the terminal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/219b5c74-f999-4bb7-9e13-59c6ade9da46">NegotiateExtVersion</a>
</td>
<td align="left" width="63%">
Negotiates an extension version to use with the specified line device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca58c796-d843-48c3-9eac-ca126395d448">put_EventFilter</a>
</td>
<td align="left" width="63%">
Sets event filters for this address.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>
 

 

