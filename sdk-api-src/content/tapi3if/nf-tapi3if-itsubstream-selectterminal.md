---
UID: NF:tapi3if.ITSubStream.SelectTerminal
title: ITSubStream::SelectTerminal (tapi3if.h)
description: The SelectTerminal method selects an ITTerminal object onto the substream. See the Remarks section under ITStream::SelectTerminal for additional information.
helpviewer_keywords: ["ITSubStream interface [TAPI 2.2]","SelectTerminal method","ITSubStream.SelectTerminal","ITSubStream::SelectTerminal","SelectTerminal","SelectTerminal method [TAPI 2.2]","SelectTerminal method [TAPI 2.2]","ITSubStream interface","_tapi3_itsubstream_selectterminal","tapi3.itsubstream_selectterminal","tapi3if/ITSubStream::SelectTerminal"]
old-location: tapi3\itsubstream_selectterminal.htm
tech.root: tapi3
ms.assetid: 5dc558ab-7422-4106-831e-9d2812530e0a
ms.date: 12/05/2018
ms.keywords: ITSubStream interface [TAPI 2.2],SelectTerminal method, ITSubStream.SelectTerminal, ITSubStream::SelectTerminal, SelectTerminal, SelectTerminal method [TAPI 2.2], SelectTerminal method [TAPI 2.2],ITSubStream interface, _tapi3_itsubstream_selectterminal, tapi3.itsubstream_selectterminal, tapi3if/ITSubStream::SelectTerminal
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
 - ITSubStream::SelectTerminal
 - tapi3if/ITSubStream::SelectTerminal
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
 - ITSubStream.SelectTerminal
---

# ITSubStream::SelectTerminal


## -description

The 
<b>SelectTerminal</b> method selects an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> object onto the substream. See the Remarks section under 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-selectterminal">ITStream::SelectTerminal</a> for additional information.

## -parameters

### -param pTerminal [in]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface of selected terminal.

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
<dt><b>TAPI_E_MAXTERMINALS</b></dt>
</dl>
</td>
<td width="60%">
Multiple terminals have been selected on the substream, but media mixing or splitting is not possible.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_INVALIDTERMINAL</b></dt>
</dl>
</td>
<td width="60%">
The terminal selected is not valid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-selectterminal">ITStream::SelectTerminal</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubStream</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>