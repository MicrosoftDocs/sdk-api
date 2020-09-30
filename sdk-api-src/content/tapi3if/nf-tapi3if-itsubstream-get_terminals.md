---
UID: NF:tapi3if.ITSubStream.get_Terminals
title: ITSubStream::get_Terminals (tapi3if.h)
description: The get_Terminals method creates a collection of terminals associated with the current substream. Provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the EnumerateTerminals method.
helpviewer_keywords: ["ITSubStream interface [TAPI 2.2]","get_Terminals method","ITSubStream.get_Terminals","ITSubStream::get_Terminals","_tapi3_itsubstream_get_terminals","get_Terminals","get_Terminals method [TAPI 2.2]","get_Terminals method [TAPI 2.2]","ITSubStream interface","tapi3.itsubstream_get_terminals","tapi3if/ITSubStream::get_Terminals"]
old-location: tapi3\itsubstream_get_terminals.htm
tech.root: tapi3
ms.assetid: 100854aa-78de-4395-9081-3b1f845c254c
ms.date: 12/05/2018
ms.keywords: ITSubStream interface [TAPI 2.2],get_Terminals method, ITSubStream.get_Terminals, ITSubStream::get_Terminals, _tapi3_itsubstream_get_terminals, get_Terminals, get_Terminals method [TAPI 2.2], get_Terminals method [TAPI 2.2],ITSubStream interface, tapi3.itsubstream_get_terminals, tapi3if/ITSubStream::get_Terminals
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
 - ITSubStream::get_Terminals
 - tapi3if/ITSubStream::get_Terminals
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
 - ITSubStream.get_Terminals
---

# ITSubStream::get_Terminals


## -description

The 
<b>get_Terminals</b> method creates a collection of terminals associated with the current substream. Provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-enumerateterminals">EnumerateTerminals</a> method.

## -parameters

### -param pTerminals [out]

Pointer to <b>VARIANT</b> containing an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface pointers (terminal objects).

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

This method returns only the terminals selected on the substream. Other terminals may be selected on the stream or on other substreams within the stream; those terminals are not returned.

TAPI calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface returned by <b>ITSubStream::get_Terminals</b>. The application must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the 
<b>ITTerminal</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubStream</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>