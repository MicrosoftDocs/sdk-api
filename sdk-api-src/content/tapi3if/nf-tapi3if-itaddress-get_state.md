---
UID: NF:tapi3if.ITAddress.get_State
title: ITAddress::get_State
author: windows-sdk-content
description: The get_State method gets the current state of the address in pAddressState.
old-location: tapi3\itaddress_get_state.htm
old-project: tapi
ms.assetid: f68d0fb0-126d-4464-9d5a-0ffae4d40cb7
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: ITAddress interface [TAPI 2.2],get_State method, ITAddress.get_State, ITAddress::get_State, _tapi3_itaddress_get_state, get_State, get_State method [TAPI 2.2], get_State method [TAPI 2.2],ITAddress interface, tapi3.itaddress_get_state, tapi3if/ITAddress::get_State
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAddress.get_State
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAddress::get_State


## -description


The 
<b>get_State</b> method gets the current state of the address in <i>pAddressState</i>.


## -parameters




### -param pAddressState [out]

Pointer to a member of 
<a href="https://msdn.microsoft.com/7c79bd68-5f1d-4796-a16b-fd786345cffd">ADDRESS_STATE</a>.


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
The <i>pAddressState</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/7c79bd68-5f1d-4796-a16b-fd786345cffd">ADDRESS_STATE</a>



<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>
 

 

