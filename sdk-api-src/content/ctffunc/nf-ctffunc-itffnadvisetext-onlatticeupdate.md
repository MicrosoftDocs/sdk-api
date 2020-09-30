---
UID: NF:ctffunc.ITfFnAdviseText.OnLatticeUpdate
title: ITfFnAdviseText::OnLatticeUpdate (ctffunc.h)
description: ITfFnAdviseText::OnLatticeUpdate method
helpviewer_keywords: ["ITfFnAdviseText interface [Text Services Framework]","OnLatticeUpdate method","ITfFnAdviseText.OnLatticeUpdate","ITfFnAdviseText::OnLatticeUpdate","OnLatticeUpdate","OnLatticeUpdate method [Text Services Framework]","OnLatticeUpdate method [Text Services Framework]","ITfFnAdviseText interface","_tsf_itffnadvisetext_onlatticeupdate_ref","ctffunc/ITfFnAdviseText::OnLatticeUpdate","tsf.itffnadvisetext_onlatticeupdate"]
old-location: tsf\itffnadvisetext_onlatticeupdate.htm
tech.root: TSF
ms.assetid: c58f3d2f-ad74-43a7-a8a8-65d65d603611
ms.date: 12/05/2018
ms.keywords: ITfFnAdviseText interface [Text Services Framework],OnLatticeUpdate method, ITfFnAdviseText.OnLatticeUpdate, ITfFnAdviseText::OnLatticeUpdate, OnLatticeUpdate, OnLatticeUpdate method [Text Services Framework], OnLatticeUpdate method [Text Services Framework],ITfFnAdviseText interface, _tsf_itffnadvisetext_onlatticeupdate_ref, ctffunc/ITfFnAdviseText::OnLatticeUpdate, tsf.itffnadvisetext_onlatticeupdate
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
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfFnAdviseText::OnLatticeUpdate
 - ctffunc/ITfFnAdviseText::OnLatticeUpdate
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
 - ITfFnAdviseText.OnLatticeUpdate
---

# ITfFnAdviseText::OnLatticeUpdate


## -description

Called when a lattice element within a context changes.

## -parameters

### -param pRange [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> object that represents the range of text that changed.

### -param pLattice [in]

Pointer to an <a href="/windows/desktop/api/ctffunc/nn-ctffunc-itflmlattice">ITfLMLattice</a> object that represents the new lattice element.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itffnadvisetext">ITfFnAdviseText</a>



<a href="/windows/desktop/api/ctffunc/nn-ctffunc-itflmlattice">ITfLMLattice</a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange
      </a>