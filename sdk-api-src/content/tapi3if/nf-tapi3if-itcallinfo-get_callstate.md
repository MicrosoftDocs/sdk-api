---
UID: NF:tapi3if.ITCallInfo.get_CallState
title: ITCallInfo::get_CallState
author: windows-sdk-content
description: The get_CallState method gets a pointer to the current call state, such as CS_IDLE.
old-location: tapi3\itcallinfo_get_callstate.htm
tech.root: tapi
ms.assetid: f7beb48f-d7d2-4a99-8e6a-6122059c9170
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITCallInfo interface [TAPI 2.2],get_CallState method, ITCallInfo.get_CallState, ITCallInfo::get_CallState, _tapi3_itcallinfo_get_callstate, get_CallState, get_CallState method [TAPI 2.2], get_CallState method [TAPI 2.2],ITCallInfo interface, tapi3.itcallinfo_get_callstate, tapi3if/ITCallInfo::get_CallState
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
 - ITCallInfo.get_CallState
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
- ITCallInfo.get_CallState
: 
---

# ITCallInfo::get_CallState


## -description


The 
<b>get_CallState</b> method gets a pointer to the current 
<a href="https://msdn.microsoft.com/d4ed5e99-3abe-4434-9f99-5e98d8c6f3f1">call state</a>, such as CS_IDLE.


## -parameters




### -param pCallState [out]

Pointer to variable containing current 
<a href="https://msdn.microsoft.com/d4ed5e99-3abe-4434-9f99-5e98d8c6f3f1">CALL_STATE</a> type.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pCallState</i> parameter is not a valid pointer.

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



<b>TAPI 2.1 Cross-References:  </b><a href="https://msdn.microsoft.com/f056bea6-aeb0-4c18-8e3b-c1c6fd907f62">LINECALLSTATUS</a>, <a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>, <b>dwMediaMode</b> member of <a href="https://msdn.microsoft.com/b077546b-cc95-44ce-99ee-f0007fd916b2">LINECALLINFO</a> structure, <a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>





## -see-also




<a href="https://msdn.microsoft.com/d4ed5e99-3abe-4434-9f99-5e98d8c6f3f1">CALL_STATE</a>



<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>
 

 

