---
UID: NF:tapi3if.ITAddress.get_Calls
title: ITAddress::get_Calls
author: windows-sdk-content
description: The get_Calls method creates a collection of calls currently active on the address. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the EnumerateCalls method.
old-location: tapi3\itaddress_get_calls.htm
tech.root: tapi
ms.assetid: b0b16578-0530-4ff9-a7ce-d36527ed2da9
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ITAddress interface [TAPI 2.2],get_Calls method, ITAddress.get_Calls, ITAddress::get_Calls, _tapi3_itaddress_get_calls, get_Calls, get_Calls method [TAPI 2.2], get_Calls method [TAPI 2.2],ITAddress interface, tapi3.itaddress_get_calls, tapi3if/ITAddress::get_Calls
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
 - ITAddress.get_Calls
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAddress::get_Calls


## -description


The 
<b>get_Calls</b> method creates a collection of calls currently active on the address. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="https://msdn.microsoft.com/2ffa90bf-3005-4fd0-b52f-b155c8b2194f">EnumerateCalls</a> method.


## -parameters




### -param pVariant [out]

Pointer to a <b>VARIANT</b> containing an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface pointers (call objects).


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pVariant</i> parameter is not a valid pointer.

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



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface returned by ITAddress::get_Calls. The application must call <b>Release</b> on the 
<b>ITCallInfo</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/2ffa90bf-3005-4fd0-b52f-b155c8b2194f">EnumerateCalls</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>



<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a>
 

 

