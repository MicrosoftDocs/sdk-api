---
UID: NF:tapi3if.ITSubStream.UnselectTerminal
title: ITSubStream::UnselectTerminal (tapi3if.h)
description: The UnselectTerminal method unselects the terminal from the substream.
helpviewer_keywords: ["ITSubStream interface [TAPI 2.2]","UnselectTerminal method","ITSubStream.UnselectTerminal","ITSubStream::UnselectTerminal","UnselectTerminal","UnselectTerminal method [TAPI 2.2]","UnselectTerminal method [TAPI 2.2]","ITSubStream interface","_tapi3_itsubstream_unselectterminal","tapi3.itsubstream_unselectterminal","tapi3if/ITSubStream::UnselectTerminal"]
old-location: tapi3\itsubstream_unselectterminal.htm
tech.root: tapi3
ms.assetid: a1b84377-bb1f-4e88-aca5-91105ff2ad6a
ms.date: 12/05/2018
ms.keywords: ITSubStream interface [TAPI 2.2],UnselectTerminal method, ITSubStream.UnselectTerminal, ITSubStream::UnselectTerminal, UnselectTerminal, UnselectTerminal method [TAPI 2.2], UnselectTerminal method [TAPI 2.2],ITSubStream interface, _tapi3_itsubstream_unselectterminal, tapi3.itsubstream_unselectterminal, tapi3if/ITSubStream::UnselectTerminal
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITSubStream::UnselectTerminal
 - tapi3if/ITSubStream::UnselectTerminal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - ITSubStream.UnselectTerminal
---

# ITSubStream::UnselectTerminal


## -description

The 
<b>UnselectTerminal</b> method unselects the terminal from the substream.

## -parameters

### -param pTerminal [in]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface terminal to remove from stream.

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

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubStream</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>