---
UID: NF:msctf.ITfContextComposition.FindComposition
title: ITfContextComposition::FindComposition (msctf.h)
description: ITfContextComposition::FindComposition method
old-location: tsf\itfcontextcomposition_findcomposition.htm
tech.root: TSF
ms.assetid: f5a7bd54-3b8f-44fd-ae6e-1415cc69c49e
ms.date: 12/05/2018
ms.keywords: FindComposition, FindComposition method [Text Services Framework], FindComposition method [Text Services Framework],ITfContextComposition interface, ITfContextComposition interface [Text Services Framework],FindComposition method, ITfContextComposition.FindComposition, ITfContextComposition::FindComposition, _tsf_itfcontextcomposition_findcomposition_ref, msctf/ITfContextComposition::FindComposition, tsf.itfcontextcomposition_findcomposition
ms.topic: method
f1_keywords:
- msctf/ITfContextComposition.FindComposition
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Msctf.dll
api_name:
- ITfContextComposition.FindComposition
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfContextComposition::FindComposition


## -description




## -parameters




### -param ecRead [in]

Contains an edit cookie that identifies the edit context. This is obtained from <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession</a>.


### -param pTestRange [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> object that specifies the range to search. This parameter can be <b>NULL</b>. If this parameter is <b>NULL</b>, the enumerator will contain all compositions in the edit context.


### -param ppEnum [out]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-ienumitfcompositionview">IEnumITfCompositionView</a> interface pointer that receives the enumerator object.


## -returns



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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The enumerator object cannot be initialized.

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
The enumerator object cannot be created.

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
</table>
 

The edit context identified by <i>ecRead</i> does not have a read-only lock.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-ienumitfcompositionview">IEnumITfCompositionView
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcontextcomposition">ITfContextComposition</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfeditsession-doeditsession">ITfEditSession::DoEditSession
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange
      </a>
 

 

