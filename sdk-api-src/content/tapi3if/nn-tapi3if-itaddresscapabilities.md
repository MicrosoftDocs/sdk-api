---
UID: NN:tapi3if.ITAddressCapabilities
title: ITAddressCapabilities
author: windows-sdk-content
description: The ITAddressCapabilities interface is used to obtain information about an address's capabilities. It is on the Address object, and an application can access it by calling QueryInterface on the Address object.
old-location: tapi3\itaddresscapabilities.htm
tech.root: tapi
ms.assetid: 36f452ce-9171-41da-b003-4c7df17790da
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITAddressCapabilities, ITAddressCapabilities interface [TAPI 2.2], ITAddressCapabilities interface [TAPI 2.2],described, _tapi3_itaddresscapabilities, tapi3.itaddresscapabilities, tapi3if/ITAddressCapabilities
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITAddressCapabilities
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAddressCapabilities interface


## -description


The 
<b>ITAddressCapabilities</b> interface is used to obtain information about an address's capabilities. It is on the Address object, and an application can access it by calling <b>QueryInterface</b> on the Address object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAddressCapabilities</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITAddressCapabilities</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/34a967ba-7d1f-4841-95be-9e83f927379b">EnumerateCallTreatments</a>
</td>
<td align="left" width="63%">
Gets call treatments. This method is provided for applications written in C/C++ and Java.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7a3eb72-6c9f-4164-a082-8b0951733dcb">EnumerateCompletionMessages</a>
</td>
<td align="left" width="63%">
Gets completion messages. This method is provided for applications written in C/C++ and Java.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33cc965f-0603-40b0-95bb-9b16025dd2b6">EnumerateDeviceClasses</a>
</td>
<td align="left" width="63%">
Gets device classes. This method is provided for applications written in C/C++ and Java.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76e61d5e-48b6-4b9c-9076-bd20a794859c">get_AddressCapability</a>
</td>
<td align="left" width="63%">
Gets the capability value for a given 
<a href="https://msdn.microsoft.com/47ddd1fb-dc47-4822-87b8-9944491f8b3e">ADDRESS_CAPABILITY</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ec4c25e-700b-4aed-97ff-e7cb420fdf96">get_AddressCapabilityString</a>
</td>
<td align="left" width="63%">
Gets the capability string for a given 
<a href="https://msdn.microsoft.com/c0afe710-ae6d-4f32-a691-956f8d6fea05">ADDRESS_CAPABILITY_STRING</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd6bbbf0-1f33-4e4f-bd81-7854019a0225">get_CallTreatments</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://msdn.microsoft.com/c28c9200-dd51-48b2-905c-fbe37c83b00f">call treatment</a>. This method is provided for Automation client applications, such as those written in Visual Basic and scripting languages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b2d9065-e519-4e76-b6a0-b62e19ecaf70">get_CompletionMessages</a>
</td>
<td align="left" width="63%">
Gets completion messages. This method is provided for Automation client applications, such as those written in Visual Basic and scripting languages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34c662c6-4166-470f-aaaf-001da4ed048a">get_DeviceClasses</a>
</td>
<td align="left" width="63%">
Gets 
<a href="https://msdn.microsoft.com/859979a8-0d16-4b7b-b183-d6e30f3e034d">device classes</a>. This method is provided for Automation client applications, such as those written in Visual Basic and scripting languages.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

