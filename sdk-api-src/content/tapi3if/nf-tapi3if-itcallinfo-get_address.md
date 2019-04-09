---
UID: NF:tapi3if.ITCallInfo.get_Address
title: ITCallInfo::get_Address (tapi3if.h)
author: windows-sdk-content
description: The get_Address method gets a pointer to the ITAddress interface of the Address object.
old-location: tapi3\itcallinfo_get_address.htm
tech.root: Tapi
ms.assetid: 40f20f33-166f-4df7-9c9f-b7436958d16a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITCallInfo interface [TAPI 2.2],get_Address method, ITCallInfo.get_Address, ITCallInfo::get_Address, _tapi3_itcallinfo_get_address, get_Address, get_Address method [TAPI 2.2], get_Address method [TAPI 2.2],ITCallInfo interface, tapi3.itcallinfo_get_address, tapi3if/ITCallInfo::get_Address
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
 - ITCallInfo.get_Address
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCallInfo::get_Address


## -description


The 
<b>get_Address</b> method gets a pointer to the 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a> interface of the 
<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address object</a>.


## -parameters




### -param ppAddress [out]

Pointer to 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a> interface.


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
The <i>ppAddress</i> parameter is not a valid pointer.

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
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a> interface returned by <b>ITCallInfo::get_Address</b>. The application must call <b>Release</b> on the 
<b>ITAddress</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address object</a>



<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>
 

 

