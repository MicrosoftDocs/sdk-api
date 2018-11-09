---
UID: NF:tapi3if.ITTerminal.get_Direction
title: ITTerminal::get_Direction
author: windows-sdk-content
description: The get_Direction method gets a TERMINAL_DIRECTION descriptor of the media stream direction for the terminal.
old-location: tapi3\itterminal_get_direction.htm
tech.root: tapi
ms.assetid: e0a69c3d-1780-4088-8249-961788dbf184
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ITTerminal interface [TAPI 2.2],get_Direction method, ITTerminal.get_Direction, ITTerminal::get_Direction, _tapi3_itterminal_get_direction, get_Direction, get_Direction method [TAPI 2.2], get_Direction method [TAPI 2.2],ITTerminal interface, tapi3.itterminal_get_direction, tapi3if/ITTerminal::get_Direction
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
 - ITTerminal.get_Direction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTerminal::get_Direction


## -description


The 
<b>get_Direction</b> method gets a 
<a href="https://msdn.microsoft.com/55ef9df3-1b85-439b-8ecb-28e5069390b9">TERMINAL_DIRECTION</a> descriptor of the media stream direction for the terminal.


## -parameters




### -param pDirection [out]


<a href="https://msdn.microsoft.com/55ef9df3-1b85-439b-8ecb-28e5069390b9">TERMINAL_DIRECTION</a> descriptor of the media stream direction for the terminal.


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
The <i>pDirection</i> parameter is not a valid pointer.

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



<a href="https://msdn.microsoft.com/55ef9df3-1b85-439b-8ecb-28e5069390b9">TERMINAL_DIRECTION</a>



<a href="https://msdn.microsoft.com/0d96f229-76c0-46a3-bc4b-6f558b9956c6">Terminal Object</a>



<a href="https://msdn.microsoft.com/08320d1c-1400-4746-b526-74b0789c5fc0">Terminal Object Interfaces</a>
 

 

