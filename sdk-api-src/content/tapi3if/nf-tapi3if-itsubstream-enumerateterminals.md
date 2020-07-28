---
UID: NF:tapi3if.ITSubStream.EnumerateTerminals
title: ITSubStream::EnumerateTerminals (tapi3if.h)
description: The EnumerateTerminals method enumerates terminals selected on the substream. Provided for C and C++ applications. Automation client applications such as Visual Basic must use the get_Terminals method.
helpviewer_keywords: ["EnumerateTerminals","EnumerateTerminals method [TAPI 2.2]","EnumerateTerminals method [TAPI 2.2]","ITSubStream interface","ITSubStream interface [TAPI 2.2]","EnumerateTerminals method","ITSubStream.EnumerateTerminals","ITSubStream::EnumerateTerminals","_tapi3_itsubstream_enumerateterminals","tapi3.itsubstream_enumerateterminals","tapi3if/ITSubStream::EnumerateTerminals"]
old-location: tapi3\itsubstream_enumerateterminals.htm
tech.root: tapi3
ms.assetid: bf5e1f7f-3820-433e-b71f-53798c202593
ms.date: 12/05/2018
ms.keywords: EnumerateTerminals, EnumerateTerminals method [TAPI 2.2], EnumerateTerminals method [TAPI 2.2],ITSubStream interface, ITSubStream interface [TAPI 2.2],EnumerateTerminals method, ITSubStream.EnumerateTerminals, ITSubStream::EnumerateTerminals, _tapi3_itsubstream_enumerateterminals, tapi3.itsubstream_enumerateterminals, tapi3if/ITSubStream::EnumerateTerminals
f1_keywords:
- tapi3if/ITSubStream.EnumerateTerminals
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
- ITSubStream.EnumerateTerminals
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITSubStream::EnumerateTerminals


## -description


The 
<b>EnumerateTerminals</b> method enumerates terminals selected on the substream. Provided for C and C++ applications. Automation client applications such as Visual Basic must use the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itstream-get_terminals">get_Terminals</a> method.


## -parameters




### -param ppEnumTerminal [out]

Pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal">IEnumTerminal</a> terminal enumerator.


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
The <i>ppEnumTerminal</i> parameter is not a valid pointer.

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

TAPI calls the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal">IEnumTerminal</a> interface returned by <b>ITSubStream::EnumerateTerminals</b>. The application must call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the 
<b>IEnumTerminal</b> interface to free resources associated with it.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal">IEnumTerminal</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubStream</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
 

 

