---
UID: NF:tapi3if.ITCallMediaEvent.get_Terminal
title: ITCallMediaEvent::get_Terminal (tapi3if.h)
author: windows-sdk-content
description: The get_Terminal method gets the terminal associated with the event.
old-location: tapi3\itcallmediaevent_get_terminal.htm
tech.root: Tapi
ms.assetid: 49fa442a-d4b0-4f51-b14a-c7819e06dcef
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITCallMediaEvent interface [TAPI 2.2],get_Terminal method, ITCallMediaEvent.get_Terminal, ITCallMediaEvent::get_Terminal, _tapi3_itcallmediaevent_get_terminal, get_Terminal, get_Terminal method [TAPI 2.2], get_Terminal method [TAPI 2.2],ITCallMediaEvent interface, tapi3.itcallmediaevent_get_terminal, tapi3if/ITCallMediaEvent::get_Terminal
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
 - ITCallMediaEvent.get_Terminal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITCallMediaEvent::get_Terminal


## -description


The 
<b>get_Terminal</b> method gets the terminal associated with the event.


## -parameters




### -param ppTerminal [out]

Pointer to 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface.


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
The <i>ppTerminal</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface returned by <b>ITCallMediaEvent::get_Terminal</b>. The application must call <b>Release</b> on 
<b>ITTerminal</b> to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/67c063ba-8b12-40d6-9011-923bdee8b214">Call Object</a>



<a href="https://msdn.microsoft.com/db55ff03-9271-4a94-9cba-a3ef0282b7b6">ITCallMediaEvent</a>



<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>
 

 

