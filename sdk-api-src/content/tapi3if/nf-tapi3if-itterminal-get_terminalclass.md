---
UID: NF:tapi3if.ITTerminal.get_TerminalClass
title: ITTerminal::get_TerminalClass
author: windows-sdk-content
description: The get_TerminalClass method gets the Terminal Class of the terminal.
old-location: tapi3\itterminal_get_terminalclass.htm
tech.root: tapi
ms.assetid: a31543da-4cb8-4719-8e33-fcb4d9d630b1
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: ITTerminal interface [TAPI 2.2],get_TerminalClass method, ITTerminal.get_TerminalClass, ITTerminal::get_TerminalClass, _tapi3_itterminal_get_terminalclass, get_TerminalClass, get_TerminalClass method [TAPI 2.2], get_TerminalClass method [TAPI 2.2],ITTerminal interface, tapi3.itterminal_get_terminalclass, tapi3if/ITTerminal::get_TerminalClass
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
 - ITTerminal.get_TerminalClass
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTerminal::get_TerminalClass


## -description


The 
<b>get_TerminalClass</b> method gets the 
<a href="https://msdn.microsoft.com/2a16d33c-2d87-4172-a5ff-33ff62e96615">Terminal Class</a> of the terminal.


## -parameters




### -param ppTerminalClass [out]

Pointer to <b>BSTR</b> representation of the 
<a href="https://msdn.microsoft.com/2a16d33c-2d87-4172-a5ff-33ff62e96615">Terminal Class</a> of the terminal.


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
The <i>ppTerminalClass</i> parameter is not a valid pointer.

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
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory allocated for the <i>ppTerminalClass</i> parameter.
			




## -see-also




<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>



<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>



<a href="https://msdn.microsoft.com/08320d1c-1400-4746-b526-74b0789c5fc0">Terminal Object Interfaces</a>
 

 

