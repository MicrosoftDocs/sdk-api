---
UID: NF:msctf.ITfContextComposition.StartComposition
title: ITfContextComposition::StartComposition (msctf.h)
description: ITfContextComposition::StartComposition method
helpviewer_keywords: ["ITfContextComposition interface [Text Services Framework]","StartComposition method","ITfContextComposition.StartComposition","ITfContextComposition::StartComposition","StartComposition","StartComposition method [Text Services Framework]","StartComposition method [Text Services Framework]","ITfContextComposition interface","_tsf_itfcontextcomposition_startcomposition_ref","msctf/ITfContextComposition::StartComposition","tsf.itfcontextcomposition_startcomposition"]
old-location: tsf\itfcontextcomposition_startcomposition.htm
tech.root: TSF
ms.assetid: aab84e6c-39c7-438e-b4f0-1d174473aa02
ms.date: 12/05/2018
ms.keywords: ITfContextComposition interface [Text Services Framework],StartComposition method, ITfContextComposition.StartComposition, ITfContextComposition::StartComposition, StartComposition, StartComposition method [Text Services Framework], StartComposition method [Text Services Framework],ITfContextComposition interface, _tsf_itfcontextcomposition_startcomposition_ref, msctf/ITfContextComposition::StartComposition, tsf.itfcontextcomposition_startcomposition
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
 - ITfContextComposition::StartComposition
 - msctf/ITfContextComposition::StartComposition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfContextComposition.StartComposition
---

# ITfContextComposition::StartComposition


## -description

Creates a new composition.

## -parameters

### -param ecWrite [in]

Contains an edit cookie that identifies the edit context. This is obtained from <a href="/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.

### -param pCompositionRange [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> object that specifies the text that the composition initially covers.

### -param pSink [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfcompositionsink">ITfCompositionSink</a> object that receives composition event notifications. This parameter is optional and can be <b>NULL</b>. If supplied, the object is released when the composition is terminated.

### -param ppComposition [out]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfcomposition">ITfComposition</a> interface pointer that receives the new composition object. This parameter receives <b>NULL</b> if the context owner rejects the composition.

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
The method was successful. If the context owner composition advise sink rejects the composition, <i>ppComposition</i> is set to <b>NULL</b>.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The composition object cannot be created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method was called within another composition operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The context object is not on a document stack.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The edit context identified by <i>ecWrite</i> does not have a read/write lock.

</td>
</tr>
</table>

## -remarks

If the context owner has installed a context owner composition advise sink, the <a href="/windows/desktop/api/msctf/nf-msctf-itfcontextownercompositionsink-onstartcomposition">ITfContextOwnerCompositionSink::OnStartComposition</a> method is called. If the advise sink rejects the new composition, this method returns S_OK but <i>ppComposition</i> is set to <b>NULL</b>.

Any text covered by <i>pCompositionRange</i> receives the GUID_PROP_COMPOSING property.

## -see-also

[IEnumITfCompositionView interface](nn-msctf-ienumitfcompositionview.md), [ITfContextComposition interface](nn-msctf-itfcontextcomposition.md), [ITfRange interface](nn-msctf-itfrange.md), [ITfCompositionSink interface](nn-msctf-itfcompositionsink.md), [ITfContextOwnerCompositionSink::OnStartComposition](nf-msctf-itfcontextownercompositionsink-onstartcomposition.md), [ITfEditSession::DoEditSession](nf-msctf-itfeditsession-doeditsession.md)