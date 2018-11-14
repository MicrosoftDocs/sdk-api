---
UID: NF:tapi3if.ITAddress.get_DoNotDisturb
title: ITAddress::get_DoNotDisturb
author: windows-sdk-content
description: The get_DoNotDisturb method gets the current status of the do not disturb feature on the address. The do not disturb feature may not be available on all addresses.
old-location: tapi3\itaddress_get_donotdisturb.htm
tech.root: tapi
ms.assetid: d9257201-bcd1-4d6b-9bc7-24b323cd4f15
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITAddress interface [TAPI 2.2],get_DoNotDisturb method, ITAddress.get_DoNotDisturb, ITAddress::get_DoNotDisturb, _tapi3_itaddress_get_donotdisturb, get_DoNotDisturb, get_DoNotDisturb method [TAPI 2.2], get_DoNotDisturb method [TAPI 2.2],ITAddress interface, tapi3.itaddress_get_donotdisturb, tapi3if/ITAddress::get_DoNotDisturb
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITAddress.get_DoNotDisturb
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tapi3if.h
: 
- ITAddress.get_DoNotDisturb
: 
---

# ITAddress::get_DoNotDisturb


## -description


The 
<b>get_DoNotDisturb</b> method gets the current status of the do not disturb feature on the address. The do not disturb feature may not be available on all addresses.


## -parameters




### -param pfDoNotDisturb [out]

If VARIANT_TRUE, the do not disturb feature has been activated. If VARIANT_FALSE, the do not disturb feature is not active.


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
<dt><b>E_OPERATIONUNAVAIL</b></dt>
</dl>
</td>
<td width="60%">
Operation unavailable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This operation is not supported on this address.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pfDoNotDisturb</i> parameter is not a valid pointer.

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
 




## -remarks



For programmers familiar with TAPI 2.<i>x:</i> The DoNotDisturb feature is implemented using the "forward" feature, if present on the address. When 
<b>get_DoNotDisturb</b> is called, Tapi3.dll gets the 
<a href="https://msdn.microsoft.com/795aa97d-76a9-4041-b9f6-345644561043">LINEADDRESSSTATUS</a> of the address object, and looks for its 
<a href="https://msdn.microsoft.com/cbdb4409-a51a-4ddf-b3ec-c5b958fc2527">LINEFORWARD</a> entries. If one such entry is found and if its <i>dwDestAddressOffset</i> member is 0 (zero), then DoNotDisturb is considered to be turned ON, and therefore VARIANT_TRUE is returned as the value for this method.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/4d3071d5-055a-469d-aa17-984b8210cbea">put_DoNotDisturb</a>
 

 

