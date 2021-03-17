---
UID: NF:msctf.ITfContextOwnerCompositionServices.TerminateComposition
title: ITfContextOwnerCompositionServices::TerminateComposition (msctf.h)
description: ITfContextOwnerCompositionServices::TerminateComposition method
helpviewer_keywords: ["ITfContextOwnerCompositionServices interface [Text Services Framework]","TerminateComposition method","ITfContextOwnerCompositionServices.TerminateComposition","ITfContextOwnerCompositionServices::TerminateComposition","TerminateComposition","TerminateComposition method [Text Services Framework]","TerminateComposition method [Text Services Framework]","ITfContextOwnerCompositionServices interface","_tsf_itfcontextownercompositionservices_terminatecomposition_ref","msctf/ITfContextOwnerCompositionServices::TerminateComposition","tsf.itfcontextownercompositionservices_terminatecomposition"]
old-location: tsf\itfcontextownercompositionservices_terminatecomposition.htm
tech.root: TSF
ms.assetid: 950ba2b3-cb12-4697-a4b2-1c87373b9a23
ms.date: 12/05/2018
ms.keywords: ITfContextOwnerCompositionServices interface [Text Services Framework],TerminateComposition method, ITfContextOwnerCompositionServices.TerminateComposition, ITfContextOwnerCompositionServices::TerminateComposition, TerminateComposition, TerminateComposition method [Text Services Framework], TerminateComposition method [Text Services Framework],ITfContextOwnerCompositionServices interface, _tsf_itfcontextownercompositionservices_terminatecomposition_ref, msctf/ITfContextOwnerCompositionServices::TerminateComposition, tsf.itfcontextownercompositionservices_terminatecomposition
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfContextOwnerCompositionServices::TerminateComposition
 - msctf/ITfContextOwnerCompositionServices::TerminateComposition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfContextOwnerCompositionServices.TerminateComposition
---

# ITfContextOwnerCompositionServices::TerminateComposition


## -description

Terminates a composition.

## -parameters

### -param pComposition [in]

Pointer to a <a href="/windows/desktop/api/msctf/nn-msctf-itfcompositionview">ITfCompositionView</a> interface that represents the composition to terminate. If this value is <b>NULL</b>, all compositions in the context are terminated.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The context is not on a document stack.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
A text service currently holds a lock on the document.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
This method was called during another composition operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -remarks

A text service uses <a href="/windows/desktop/api/msctf/nf-msctf-itfcomposition-endcomposition">ITfComposition::EndComposition</a> to terminate a composition that it created.

If the context owner implements the text store, the context owner must be able to grant a synchronous write lock before calling this method.

This method also does the following:

<ul>
<li>For each composition terminated, <a href="/windows/desktop/api/msctf/nf-msctf-itfcompositionsink-oncompositionterminated">ITfCompositionSink::OnCompositionTerminated</a> is called for all installed composition advise sinks.</li>
<li>If the context owner installed a context owner composition advise sink, <a href="/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onendcomposition">ITfContextOwnerCompositionSink::OnEndComposition</a> is called for each terminated composition.</li>
<li>The GUID_PROP_COMPOSING property will be cleared for the text covered by each terminated composition.</li>
</ul>

## -see-also

[ITfComposition::EndComposition](nf-msctf-itfcomposition-endcomposition.md), [nf-msctf-itfcompositionsink-oncompositionterminated](nf-msctf-itfcompositionsink-oncompositionterminated.md), [ITfCompositionView interface](nn-msctf-itfcompositionview.md), [ITfContextOwnerCompositionServices interface](nn-msctf-itfcontextownercompositionservices.md), [ITfContextOwnerCompositionSink::OnEndComposition](nf-msctf-itfcontextownercompositionsink-onendcomposition.md)