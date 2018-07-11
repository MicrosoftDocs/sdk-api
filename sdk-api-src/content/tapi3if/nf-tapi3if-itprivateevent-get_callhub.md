---
UID: NF:tapi3if.ITPrivateEvent.get_CallHub
title: ITPrivateEvent::get_CallHub
author: windows-sdk-content
description: The get_CallHub method returns a pointer to the ITCallHub interface on which the event occurred.
old-location: tapi3\itprivateevent_get_callhub.htm
old-project: tapi
ms.assetid: c69f0c96-134f-4b78-91dc-44339aa06a98
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: ITPrivateEvent interface [TAPI 2.2],get_CallHub method, ITPrivateEvent.get_CallHub, ITPrivateEvent::get_CallHub, _tapi3_itprivateevent_get_callhub, get_CallHub, get_CallHub method [TAPI 2.2], get_CallHub method [TAPI 2.2],ITPrivateEvent interface, tapi3.itprivateevent_get_callhub, tapi3if/ITPrivateEvent::get_CallHub
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
 - ITPrivateEvent.get_CallHub
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPrivateEvent::get_CallHub


## -description


The 
<b>get_CallHub</b> method returns a pointer to the 
<a href="https://msdn.microsoft.com/bdc91cac-c0ec-4484-a415-8cd1aa1e18e8">ITCallHub</a> interface on which the event occurred.


## -parameters




### -param ppCallHub [out]

 Pointer to 
<a href="https://msdn.microsoft.com/bdc91cac-c0ec-4484-a415-8cd1aa1e18e8">ITCallHub</a> interface.


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
The <i>ppCallHub</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ea23ae25-2fbb-4060-8273-cd7921d49e52">CallHub Object</a>



<a href="https://msdn.microsoft.com/bdc91cac-c0ec-4484-a415-8cd1aa1e18e8">ITCallHub</a>



<a href="https://msdn.microsoft.com/75a711e4-21b2-40a4-81f0-a210829178b9">ITPrivateEvent</a>
 

 

