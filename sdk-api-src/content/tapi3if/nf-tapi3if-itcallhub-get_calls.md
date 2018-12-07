---
UID: NF:tapi3if.ITCallHub.get_Calls
title: ITCallHub::get_Calls
author: windows-sdk-content
description: The get_Calls method creates a collection of calls associated with the current call hub. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the EnumerateCalls method.
old-location: tapi3\itcallhub_get_calls.htm
tech.root: tapi
ms.assetid: 56634ab6-b905-48bb-a4d1-7ca1f0c4c0cf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITCallHub interface [TAPI 2.2],get_Calls method, ITCallHub.get_Calls, ITCallHub::get_Calls, _tapi3_itcallhub_get_calls, get_Calls, get_Calls method [TAPI 2.2], get_Calls method [TAPI 2.2],ITCallHub interface, tapi3.itcallhub_get_calls, tapi3if/ITCallHub::get_Calls
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
 - ITCallHub.get_Calls
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCallHub::get_Calls


## -description


The 
<b>get_Calls</b> method creates a collection of calls associated with the current call hub. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="https://msdn.microsoft.com/becacf70-0ae7-419c-a53f-c6172278d29f">EnumerateCalls</a> method.


## -parameters




### -param pCalls [out]

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
The <i>pCalls</i> parameter is not a valid pointer.

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
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a> interface returned by <b>ITCallHub::get_Calls</b>. The application must call <b>Release</b> on the 
<b>ITCallInfo</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/ea23ae25-2fbb-4060-8273-cd7921d49e52">CallHub Object</a>



<a href="https://msdn.microsoft.com/bdc91cac-c0ec-4484-a415-8cd1aa1e18e8">ITCallHub</a>



<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>



<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a>
 

 

