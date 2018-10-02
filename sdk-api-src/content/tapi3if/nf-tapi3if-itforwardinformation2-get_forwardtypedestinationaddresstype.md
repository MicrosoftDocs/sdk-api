---
UID: NF:tapi3if.ITForwardInformation2.get_ForwardTypeDestinationAddressType
title: ITForwardInformation2::get_ForwardTypeDestinationAddressType
author: windows-sdk-content
description: The get_ForwardTypeDestinationAddressType method gets the destination address type for a given forwarding type.
old-location: tapi3\itforwardinformation2_get_forwardtypedestinationaddresstype.htm
tech.root: TAPI
ms.assetid: de40538a-e2ba-49ec-bde6-6803da6515da
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITForwardInformation2 interface [TAPI 2.2],get_ForwardTypeDestinationAddressType method, ITForwardInformation2.get_ForwardTypeDestinationAddressType, ITForwardInformation2::get_ForwardTypeDestinationAddressType, _tapi3_itforwardinformation2_get_forwardtypedestinationaddresstype, get_ForwardTypeDestinationAddressType, get_ForwardTypeDestinationAddressType method [TAPI 2.2], get_ForwardTypeDestinationAddressType method [TAPI 2.2],ITForwardInformation2 interface, tapi3.itforwardinformation2_get_forwardtypedestinationaddresstype, tapi3if/ITForwardInformation2::get_ForwardTypeDestinationAddressType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ITForwardInformation2.get_ForwardTypeDestinationAddressType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITForwardInformation2::get_ForwardTypeDestinationAddressType


## -description


The 
<b>get_ForwardTypeDestinationAddressType</b> method gets the destination address type for a given forwarding type.


## -parameters




### -param ForwardType [in]


<a href="https://msdn.microsoft.com/8cc053bd-1056-42be-b48a-d2312c456893">Line forward type</a> to be retrieved.


### -param pDestAddressType [out]


<a href="https://msdn.microsoft.com/2c32eda1-e510-40eb-ae75-fc7b9e9953cd">Address type</a> of the destination.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
The <i>ForwardType</i> parameter is invalid.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pDestAddressType</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0e06cd0b-b95b-4853-b883-53146be084f0">ITForwardInformation</a>



<a href="https://msdn.microsoft.com/25c99955-1a9d-49fa-9432-962e19296ad5">ITForwardInformation2</a>



<a href="https://msdn.microsoft.com/02d3c558-585a-4dcc-873e-8465c1d2af64">ITForwardInformation::GetForwardType</a>
 

 

