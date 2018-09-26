---
UID: NF:tapi3if.ITStream.get_Terminals
title: ITStream::get_Terminals
author: windows-sdk-content
description: The get_Terminals method creates a collection of terminals associated with the current stream. Provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the EnumerateTerminals method.
old-location: tapi3\itstream_get_terminals.htm
tech.root: tapi
ms.assetid: 2861dbf7-fc13-4182-90e5-32347f3d1e54
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ITStream interface [TAPI 2.2],get_Terminals method, ITStream.get_Terminals, ITStream::get_Terminals, _tapi3_itstream_get_terminals, get_Terminals, get_Terminals method [TAPI 2.2], get_Terminals method [TAPI 2.2],ITStream interface, tapi3.itstream_get_terminals, tapi3if/ITStream::get_Terminals
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
 - ITStream.get_Terminals
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITStream::get_Terminals


## -description


The 
<b>get_Terminals</b> method creates a collection of terminals associated with the current stream. Provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="https://msdn.microsoft.com/c57af2a9-a2ec-45ba-9e10-7b5f41bdeb00">EnumerateTerminals</a> method.


## -parameters




### -param pTerminals [out]

Pointer to <b>VARIANT</b> containing an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface pointers (terminal objects).


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
The <i>pTerminals</i> parameter is not a valid pointer.

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



TAPI calls the <a href="https://msdn.microsoft.com/en-us/library/ms691379(v=VS.85).aspx">AddRef</a> method on the 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface returned by <b>ITStream::get_Terminals</b>. The application must call <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">Release</a> on the 
<b>ITTerminal</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a>



<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a>



<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

