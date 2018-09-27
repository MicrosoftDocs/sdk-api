---
UID: NF:tapi3if.ITCallHub.get_NumCalls
title: ITCallHub::get_NumCalls
author: windows-sdk-content
description: The get_NumCalls method gets the number of calls currently in the CallHub.
old-location: tapi3\itcallhub_get_numcalls.htm
tech.root: tapi
ms.assetid: 52313969-ce8e-43da-8844-b4d0834dd446
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ITCallHub interface [TAPI 2.2],get_NumCalls method, ITCallHub.get_NumCalls, ITCallHub::get_NumCalls, _tapi3_itcallhub_get_numcalls, get_NumCalls, get_NumCalls method [TAPI 2.2], get_NumCalls method [TAPI 2.2],ITCallHub interface, tapi3.itcallhub_get_numcalls, tapi3if/ITCallHub::get_NumCalls
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
 - ITCallHub.get_NumCalls
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCallHub::get_NumCalls


## -description


The 
<b>get_NumCalls</b> method gets the number of calls currently in the CallHub.


## -parameters




### -param plCalls [out]

Total number of calls in the CallHub.


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
The <i>plCalls</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ea23ae25-2fbb-4060-8273-cd7921d49e52">CallHub Object</a>



<a href="https://msdn.microsoft.com/bdc91cac-c0ec-4484-a415-8cd1aa1e18e8">ITCallHub</a>
 

 

