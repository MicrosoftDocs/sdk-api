---
UID: NF:tapi3if.ITCallHub.get_State
title: ITCallHub::get_State
author: windows-sdk-content
description: The get_State method gets the current state of the CallHub.
old-location: tapi3\itcallhub_get_state.htm
old-project: tapi
ms.assetid: 0ca4bbad-6822-4a8b-8df4-da6e630752f0
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITCallHub interface [TAPI 2.2],get_State method, ITCallHub.get_State, ITCallHub::get_State, _tapi3_itcallhub_get_state, get_State, get_State method [TAPI 2.2], get_State method [TAPI 2.2],ITCallHub interface, tapi3.itcallhub_get_state, tapi3if/ITCallHub::get_State
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.redist: 
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
 - ITCallHub.get_State
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITCallHub::get_State


## -description


The 
<b>get_State</b> method gets the current state of the CallHub.


## -parameters




### -param pState [out]

Pointer to 
<a href="https://msdn.microsoft.com/8ddfe1f5-2f4a-4b41-83ce-858a669afc31">CALLHUB_STATE</a> indicator of state.


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
The <i>pState</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8ddfe1f5-2f4a-4b41-83ce-858a669afc31">CALLHUB_STATE</a>



<a href="https://msdn.microsoft.com/ea23ae25-2fbb-4060-8273-cd7921d49e52">CallHub Object</a>



<a href="https://msdn.microsoft.com/bdc91cac-c0ec-4484-a415-8cd1aa1e18e8">ITCallHub</a>
 

 

