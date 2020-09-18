---
UID: NF:ctffunc.ITfFnAdviseText.OnTextUpdate
title: ITfFnAdviseText::OnTextUpdate (ctffunc.h)
description: ITfFnAdviseText::OnTextUpdate method
helpviewer_keywords: ["ITfFnAdviseText interface [Text Services Framework]","OnTextUpdate method","ITfFnAdviseText.OnTextUpdate","ITfFnAdviseText::OnTextUpdate","OnTextUpdate","OnTextUpdate method [Text Services Framework]","OnTextUpdate method [Text Services Framework]","ITfFnAdviseText interface","_tsf_itffnadvisetext_ontextupdate_ref","ctffunc/ITfFnAdviseText::OnTextUpdate","tsf.itffnadvisetext_ontextupdate"]
old-location: tsf\itffnadvisetext_ontextupdate.htm
tech.root: TSF
ms.assetid: 0b8235bd-22a6-4074-89e5-2223a20f3559
ms.date: 12/05/2018
ms.keywords: ITfFnAdviseText interface [Text Services Framework],OnTextUpdate method, ITfFnAdviseText.OnTextUpdate, ITfFnAdviseText::OnTextUpdate, OnTextUpdate, OnTextUpdate method [Text Services Framework], OnTextUpdate method [Text Services Framework],ITfFnAdviseText interface, _tsf_itffnadvisetext_ontextupdate_ref, ctffunc/ITfFnAdviseText::OnTextUpdate, tsf.itffnadvisetext_ontextupdate
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
 - ITfFnAdviseText::OnTextUpdate
 - ctffunc/ITfFnAdviseText::OnTextUpdate
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
 - ITfFnAdviseText.OnTextUpdate
---

# ITfFnAdviseText::OnTextUpdate


## -description

Called when the text within a context changes.

## -parameters

### -param pRange [in]

Pointer to an <a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a> object that represents the range of text that has changed.

### -param pchText [in]

Pointer to a <b>WCHAR</b> buffer that contains the new text for the range.

### -param cch [in]

Specifies the number of characters contained in <i>pchText</i>.

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



<a href="/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange
      </a>