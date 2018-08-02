---
UID: NF:tapi3if.ITStream.UnselectTerminal
title: ITStream::UnselectTerminal
author: windows-sdk-content
description: The UnselectTerminal method unselects the terminal from the stream and stops streaming for this stream.
old-location: tapi3\itstream_unselectterminal.htm
old-project: Tapi
ms.assetid: ad16ea41-0c02-4bba-bfd9-267b56c481e1
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITStream interface [TAPI 2.2],UnselectTerminal method, ITStream.UnselectTerminal, ITStream::UnselectTerminal, UnselectTerminal, UnselectTerminal method [TAPI 2.2], UnselectTerminal method [TAPI 2.2],ITStream interface, _tapi3_itstream_unselectterminal, tapi3.itstream_unselectterminal, tapi3if/ITStream::UnselectTerminal
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
 - tapi3if.h
api_name:
 - ITStream.UnselectTerminal
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITStream::UnselectTerminal


## -description


The 
<b>UnselectTerminal</b> method unselects the terminal from the stream and stops streaming for this stream.


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

Successfully unselecting the last terminal from a stream effectively ceases any existing streaming for this particular stream. Subsequently selecting the same terminal or another terminal restarts such interrupted streaming.

Reselection onto a stream with a different terminal, or a newly created one, can have unexpected effects. The filter graph may retain information from the previous terminal that fails to match the new one.




## -see-also




<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

