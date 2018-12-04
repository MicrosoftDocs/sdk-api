---
UID: NF:tapi3if.ITCallInfo.get_CallHub
title: ITCallInfo::get_CallHub
author: windows-sdk-content
description: The get_CallHub method gets a pointer to the ITCallHub interface of the CallHub object.
old-location: tapi3\itcallinfo_get_callhub.htm
tech.root: tapi
ms.assetid: ae7d74f7-c69b-45d1-a049-59e581856f27
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: ITCallInfo interface [TAPI 2.2],get_CallHub method, ITCallInfo.get_CallHub, ITCallInfo::get_CallHub, _tapi3_itcallinfo_get_callhub, get_CallHub, get_CallHub method [TAPI 2.2], get_CallHub method [TAPI 2.2],ITCallInfo interface, tapi3.itcallinfo_get_callhub, tapi3if/ITCallInfo::get_CallHub
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
 - ITCallInfo.get_CallHub
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCallInfo::get_CallHub


## -description


The 
<b>get_CallHub</b> method gets a pointer to the 
<a href="https://msdn.microsoft.com/bdc91cac-c0ec-4484-a415-8cd1aa1e18e8">ITCallHub</a> interface of the 
<a href="https://msdn.microsoft.com/ea23ae25-2fbb-4060-8273-cd7921d49e52">CallHub object</a>.


## -parameters




### -param ppCallHub [out]

Pointer to 
<a href="https://msdn.microsoft.com/bdc91cac-c0ec-4484-a415-8cd1aa1e18e8">ITCallHub</a> interface of the CallHub object.


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
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
Call hub not yet available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppCallHub</i> parameter is not a valid pointer.

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



On some service providers, the call hub is not available until after the call is made.

TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/bdc91cac-c0ec-4484-a415-8cd1aa1e18e8">ITCallHub</a> interface returned by <b>ITCallInfo::get_CallHub</b>. The application must call <b>Release</b> on the 
<b>ITCallHub</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/ea23ae25-2fbb-4060-8273-cd7921d49e52">CallHub object</a>



<a href="https://msdn.microsoft.com/bdc91cac-c0ec-4484-a415-8cd1aa1e18e8">ITCallHub</a>



<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>
 

 

