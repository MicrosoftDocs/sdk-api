---
UID: NF:ctffunc.IEnumTfLatticeElements.Next
title: IEnumTfLatticeElements::Next (ctffunc.h)
description: IEnumTfLatticeElements::Next method
helpviewer_keywords: ["IEnumTfLatticeElements interface [Text Services Framework]","Next method","IEnumTfLatticeElements.Next","IEnumTfLatticeElements::Next","Next","Next method [Text Services Framework]","Next method [Text Services Framework]","IEnumTfLatticeElements interface","_tsf_ienumtflatticeelements_next_ref","ctffunc/IEnumTfLatticeElements::Next","tsf.ienumtflatticeelements_next"]
old-location: tsf\ienumtflatticeelements_next.htm
tech.root: TSF
ms.assetid: 066493c9-6597-43f4-9f65-51578af00a9b
ms.date: 12/05/2018
ms.keywords: IEnumTfLatticeElements interface [Text Services Framework],Next method, IEnumTfLatticeElements.Next, IEnumTfLatticeElements::Next, Next, Next method [Text Services Framework], Next method [Text Services Framework],IEnumTfLatticeElements interface, _tsf_ienumtflatticeelements_next_ref, ctffunc/IEnumTfLatticeElements::Next, tsf.ienumtflatticeelements_next
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Sptip.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - IEnumTfLatticeElements::Next
 - ctffunc/IEnumTfLatticeElements::Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sptip.dll
api_name:
 - IEnumTfLatticeElements.Next
---

# IEnumTfLatticeElements::Next


## -description

Obtains the specified number of elements in the enumeration sequence from the current position.

## -parameters

### -param ulCount [in]

Specifies the number of elements to obtain.

### -param rgsElements [out]

Pointer to an array of <a href="/windows/desktop/api/ctffunc/ns-ctffunc-tf_lmlattelement">TF_LMLATTELEMENT</a> structures that receives the requested data. This array must be at least <i>ulCount</i> elements in size.

The caller must free the <b>bstrText</b> member of every structure obtained using <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> when it is no longer required.

### -param pcFetched [out]

Pointer to a ULONG value that receives the number of elements actually obtained. This value can be less than the number of items requested. This parameter can be <b>NULL</b>.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method reached the end of the enumeration before the specified number of elements could be obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>rgsElements</i> is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-ienumtflatticeelements">IEnumTfLatticeElements</a>



<a href="/windows/desktop/api/ctffunc/ns-ctffunc-tf_lmlattelement">TF_LMLATTELEMENT
      </a>