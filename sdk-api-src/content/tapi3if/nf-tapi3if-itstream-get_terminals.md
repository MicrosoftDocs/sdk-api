---
UID: NF:tapi3if.ITStream.get_Terminals
title: ITStream::get_Terminals (tapi3if.h)
description: The get_Terminals method creates a collection of terminals associated with the current stream. Provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the EnumerateTerminals method.helpviewer_keywords: ["ITStream interface [TAPI 2.2]","get_Terminals method","ITStream.get_Terminals","ITStream::get_Terminals","_tapi3_itstream_get_terminals","get_Terminals","get_Terminals method [TAPI 2.2]","get_Terminals method [TAPI 2.2]","ITStream interface","tapi3.itstream_get_terminals","tapi3if/ITStream::get_Terminals"]
old-location: tapi3\itstream_get_terminals.htm
tech.root: Tapi
ms.assetid: 2861dbf7-fc13-4182-90e5-32347f3d1e54
ms.date: 12/05/2018
ms.keywords: ITStream interface [TAPI 2.2],get_Terminals method, ITStream.get_Terminals, ITStream::get_Terminals, _tapi3_itstream_get_terminals, get_Terminals, get_Terminals method [TAPI 2.2], get_Terminals method [TAPI 2.2],ITStream interface, tapi3.itstream_get_terminals, tapi3if/ITStream::get_Terminals
f1_keywords:
- tapi3if/ITStream.get_Terminals
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITStream::get_Terminals


## -description


The 
<b>get_Terminals</b> method creates a collection of terminals associated with the current stream. Provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itstream-enumerateterminals">EnumerateTerminals</a> method.


## -parameters




### -param pTerminals [out]

Pointer to <b>VARIANT</b> containing an 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface pointers (terminal objects).


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



TAPI calls the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface returned by <b>ITStream::get_Terminals</b>. The application must call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the 
<b>ITTerminal</b> interface to free resources associated with it.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
 

 

