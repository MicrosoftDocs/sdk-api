---
UID: NF:tapi3if.ITForwardInformation2.get_ForwardTypeCallerAddressType
title: ITForwardInformation2::get_ForwardTypeCallerAddressType
author: windows-driver-content
description: The get_ForwardTypeCallerAddressType method gets the caller address type for a given forwarding type.
old-location: tapi3\itforwardinformation2_get_forwardtypecalleraddresstype.htm
old-project: Tapi
ms.assetid: 030d2b44-0c1d-488b-8cd9-e68ad6d26c6e
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ITForwardInformation2 interface [TAPI 2.2],get_ForwardTypeCallerAddressType method, ITForwardInformation2.get_ForwardTypeCallerAddressType, ITForwardInformation2::get_ForwardTypeCallerAddressType, _tapi3_itforwardinformation2_get_forwardtypecalleraddresstype, get_ForwardTypeCallerAddressType, get_ForwardTypeCallerAddressType method [TAPI 2.2], get_ForwardTypeCallerAddressType method [TAPI 2.2],ITForwardInformation2 interface, tapi3.itforwardinformation2_get_forwardtypecalleraddresstype, tapi3if/ITForwardInformation2::get_ForwardTypeCallerAddressType
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
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITForwardInformation2.get_ForwardTypeCallerAddressType
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITForwardInformation2::get_ForwardTypeCallerAddressType


## -description


The 
<b>get_ForwardTypeCallerAddressType</b> method gets the caller address type for a given forwarding type.


## -parameters




### -param Forwardtype [in]


<a href="https://msdn.microsoft.com/8cc053bd-1056-42be-b48a-d2312c456893">Line forward type</a> to be retrieved.


### -param pCallerAddressType [out]


<a href="https://msdn.microsoft.com/2c32eda1-e510-40eb-ae75-fc7b9e9953cd">Address type</a> of the caller.


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
The <i>Forwardtype</i> parameter is invalid.

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
The <i>pCallerAddressType</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0e06cd0b-b95b-4853-b883-53146be084f0">ITForwardInformation</a>



<a href="https://msdn.microsoft.com/25c99955-1a9d-49fa-9432-962e19296ad5">ITForwardInformation2</a>



<a href="https://msdn.microsoft.com/02d3c558-585a-4dcc-873e-8465c1d2af64">ITForwardInformation::GetForwardType</a>
 

 

