---
UID: NF:tapi3if.ITSubStream.UnselectTerminal
title: ITSubStream::UnselectTerminal
author: windows-sdk-content
description: The UnselectTerminal method unselects the terminal from the substream.
old-location: tapi3\itsubstream_unselectterminal.htm
tech.root: tapi
ms.assetid: a1b84377-bb1f-4e88-aca5-91105ff2ad6a
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: ITSubStream interface [TAPI 2.2],UnselectTerminal method, ITSubStream.UnselectTerminal, ITSubStream::UnselectTerminal, UnselectTerminal, UnselectTerminal method [TAPI 2.2], UnselectTerminal method [TAPI 2.2],ITSubStream interface, _tapi3_itsubstream_unselectterminal, tapi3.itsubstream_unselectterminal, tapi3if/ITSubStream::UnselectTerminal
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
 - ITSubStream.UnselectTerminal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITSubStream::UnselectTerminal


## -description


The 
<b>UnselectTerminal</b> method unselects the terminal from the substream.


## -parameters




### -param pTerminal [in]

Pointer to 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface terminal to remove from stream.


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
The <i>pTerminal</i> parameter is not a valid pointer.

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
<dt><b>TAPI_E_INVALIDTERMINAL</b></dt>
</dl>
</td>
<td width="60%">
The <i>pTerminal</i> parameter does not point to a valid terminal.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The provider does not support this operation.

</td>
</tr>
</table>
 




## -remarks



Some stream events may be received after streaming has been stopped due to delayed transmission.

Successfully unselecting the last terminal from a substream effectively ceases any existing streaming for this particular substream. Subsequently selecting the same terminal or another terminal restarts such interrupted streaming.




## -see-also




<a href="https://msdn.microsoft.com/fc495bc3-1172-4e39-b617-055b7ac95898">ITSubStream</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

