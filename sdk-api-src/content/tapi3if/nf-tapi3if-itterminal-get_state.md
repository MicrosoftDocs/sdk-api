---
UID: NF:tapi3if.ITTerminal.get_State
title: ITTerminal::get_State
author: windows-sdk-content
description: The get_State method gets the current state of the terminal.
old-location: tapi3\itterminal_get_state.htm
tech.root: tapi
ms.assetid: 18eebe2c-2c65-4836-a371-146eb76a379c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITTerminal interface [TAPI 2.2],get_State method, ITTerminal.get_State, ITTerminal::get_State, _tapi3_itterminal_get_state, get_State, get_State method [TAPI 2.2], get_State method [TAPI 2.2],ITTerminal interface, tapi3.itterminal_get_state, tapi3if/ITTerminal::get_State
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITTerminal.get_State
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTerminal::get_State


## -description


The 
<b>get_State</b> method gets the current state of the terminal.


## -parameters




### -param pTerminalState [out]

Pointer to a 
<a href="https://msdn.microsoft.com/310c41f5-dfe7-491d-8669-87a98694f5b7">TERMINAL_STATE</a> enum member.


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
The <i>pTerminalState</i> parameter is not a valid pointer.

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
 




## -see-also




<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>



<a href="https://msdn.microsoft.com/310c41f5-dfe7-491d-8669-87a98694f5b7">TERMINAL_STATE</a>



<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>



<a href="https://msdn.microsoft.com/08320d1c-1400-4746-b526-74b0789c5fc0">Terminal Object Interfaces</a>
 

 

