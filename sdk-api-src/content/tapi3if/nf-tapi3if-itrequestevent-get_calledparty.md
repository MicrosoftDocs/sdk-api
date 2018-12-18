---
UID: NF:tapi3if.ITRequestEvent.get_CalledParty
title: ITRequestEvent::get_CalledParty
author: windows-sdk-content
description: The get_CalledParty method gets the called party.
old-location: tapi3\itrequestevent_get_calledparty.htm
tech.root: tapi
ms.assetid: 0dfbf033-83cf-4e2c-b107-963c10595ee5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITRequestEvent interface [TAPI 2.2],get_CalledParty method, ITRequestEvent.get_CalledParty, ITRequestEvent::get_CalledParty, _tapi3_itrequestevent_get_calledparty, get_CalledParty, get_CalledParty method [TAPI 2.2], get_CalledParty method [TAPI 2.2],ITRequestEvent interface, tapi3.itrequestevent_get_calledparty, tapi3if/ITRequestEvent::get_CalledParty
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
 - ITRequestEvent.get_CalledParty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITRequestEvent::get_CalledParty


## -description


The 
<b>get_CalledParty</b> method gets the called party.


## -parameters




### -param ppCalledParty [out]

Pointer to a <b>BSTR</b> containing the called party identifier.


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
The <i>ppCalledParty</i> is not a valid pointer.

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



The application must use 
<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> to free the memory allocated for the <i>ppCalledParty</i> parameter.
			




## -see-also




<a href="https://msdn.microsoft.com/69f9b504-be01-4167-8002-32a8e86bab0f">ITRequestEvent</a>
 

 

