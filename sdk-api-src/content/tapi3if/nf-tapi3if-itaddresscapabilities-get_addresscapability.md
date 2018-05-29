---
UID: NF:tapi3if.ITAddressCapabilities.get_AddressCapability
title: ITAddressCapabilities::get_AddressCapability
author: windows-sdk-content
description: The get_AddressCapability method gets the capability value for a given ADDRESS_CAPABILITY.
old-location: tapi3\itaddresscapabilities_get_addresscapability.htm
old-project: Tapi
ms.assetid: 76e61d5e-48b6-4b9c-9076-bd20a794859c
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITAddressCapabilities interface [TAPI 2.2],get_AddressCapability method, ITAddressCapabilities.get_AddressCapability, ITAddressCapabilities::get_AddressCapability, _tapi3_itaddresscapabilities_get_addresscapability, get_AddressCapability, get_AddressCapability method [TAPI 2.2], get_AddressCapability method [TAPI 2.2],ITAddressCapabilities interface, tapi3.itaddresscapabilities_get_addresscapability, tapi3if/ITAddressCapabilities::get_AddressCapability
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITAddressCapabilities.get_AddressCapability
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAddressCapabilities::get_AddressCapability


## -description


The 
<b>get_AddressCapability</b> method gets the capability value for a given 
<a href="https://msdn.microsoft.com/47ddd1fb-dc47-4822-87b8-9944491f8b3e">ADDRESS_CAPABILITY</a>.


## -parameters




### -param AddressCap [in]

Descriptor for desired address capability.


### -param plCapability [out]

Value of address capability.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>AddressCap</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>plCapability</i> parameter in not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/47ddd1fb-dc47-4822-87b8-9944491f8b3e">ADDRESS_CAPABILITY</a>



<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/36f452ce-9171-41da-b003-4c7df17790da">ITAddressCapabilities</a>
 

 

