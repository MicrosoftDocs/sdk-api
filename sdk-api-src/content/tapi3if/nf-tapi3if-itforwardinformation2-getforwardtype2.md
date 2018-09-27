---
UID: NF:tapi3if.ITForwardInformation2.GetForwardType2
title: ITForwardInformation2::GetForwardType2
author: windows-sdk-content
description: The GetForwardType2 method gets the current forwarding mode, specified by caller address.
old-location: tapi3\itforwardinformation2_getforwardtype2.htm
tech.root: tapi
ms.assetid: c3142217-d3fa-4e0b-ad3b-65a0557ce951
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: GetForwardType2, GetForwardType2 method [TAPI 2.2], GetForwardType2 method [TAPI 2.2],ITForwardInformation2 interface, ITForwardInformation2 interface [TAPI 2.2],GetForwardType2 method, ITForwardInformation2.GetForwardType2, ITForwardInformation2::GetForwardType2, _tapi3_itforwardinformation2_getforwardtype2, tapi3.itforwardinformation2_getforwardtype2, tapi3if/ITForwardInformation2::GetForwardType2
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
 - ITForwardInformation2.GetForwardType2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITForwardInformation2::GetForwardType2


## -description


The 
<b>GetForwardType2</b> method gets the current forwarding mode, specified by caller address.


## -parameters




### -param ForwardType [in]


<a href="https://msdn.microsoft.com/8cc053bd-1056-42be-b48a-d2312c456893">Line forward type</a> to be retrieved.


### -param ppDestinationAddress [out]

Pointer to the <b>BSTR</b> representation of the destination address.


### -param pDestAddressType [out]


<a href="https://msdn.microsoft.com/2c32eda1-e510-40eb-ae75-fc7b9e9953cd">Address type</a> of the destination.


### -param ppCallerAddress [out]

Pointer to the <b>BSTR</b> representation of the caller address.


### -param pCallerAddressType [out]


<a href="https://msdn.microsoft.com/2c32eda1-e510-40eb-ae75-fc7b9e9953cd">Address type</a> of the caller.


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
The <i>ForwardType</i>, <i>pDestAddressType</i>, or <i>pCallerAddressType</i> parameter is invalid.

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
The <i>ppDestinationAddress</i>, <i>pDestAddressType</i>, <i>pCallerAddressType</i>, or <i>ppCallerAddress</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0e06cd0b-b95b-4853-b883-53146be084f0">ITForwardInformation</a>



<a href="https://msdn.microsoft.com/25c99955-1a9d-49fa-9432-962e19296ad5">ITForwardInformation2</a>



<a href="https://msdn.microsoft.com/02d3c558-585a-4dcc-873e-8465c1d2af64">ITForwardInformation::GetForwardType</a>
 

 

