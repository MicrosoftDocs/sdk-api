---
UID: NF:msctf.ITfThreadMgr.AssociateFocus
title: ITfThreadMgr::AssociateFocus (msctf.h)
description: ITfThreadMgr::AssociateFocus method
helpviewer_keywords: ["AssociateFocus","AssociateFocus method [Text Services Framework]","AssociateFocus method [Text Services Framework]","ITfThreadMgr interface","ITfThreadMgr interface [Text Services Framework]","AssociateFocus method","ITfThreadMgr.AssociateFocus","ITfThreadMgr::AssociateFocus","_tsf_itfthreadmgr_associatefocus_ref","msctf/ITfThreadMgr::AssociateFocus","tsf.itfthreadmgr_associatefocus"]
old-location: tsf\itfthreadmgr_associatefocus.htm
tech.root: TSF
ms.assetid: e2e0ef4e-5254-42c3-aebf-9d46cdee7e67
ms.date: 12/05/2018
ms.keywords: AssociateFocus, AssociateFocus method [Text Services Framework], AssociateFocus method [Text Services Framework],ITfThreadMgr interface, ITfThreadMgr interface [Text Services Framework],AssociateFocus method, ITfThreadMgr.AssociateFocus, ITfThreadMgr::AssociateFocus, _tsf_itfthreadmgr_associatefocus_ref, msctf/ITfThreadMgr::AssociateFocus, tsf.itfthreadmgr_associatefocus
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ITfThreadMgr::AssociateFocus
 - msctf/ITfThreadMgr::AssociateFocus
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
 - ITfThreadMgr.AssociateFocus
---

# ITfThreadMgr::AssociateFocus


## -description

Associates the focus for a window with a document manager object.

## -parameters

### -param hwnd [in]

Handle of the window to associate the focus with.

### -param pdimNew [in]

Pointer to the document manager to associate the focus with. The TSF manager does not increment the object reference count. This value can be <b>NULL</b>.

### -param ppdimPrev [out]

Receives the document manager previously associated with the window. Receives <b>NULL</b> if there is no previous association. This parameter cannot be <b>NULL</b>.

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

## -remarks

This method is provided as a convenience to the application developer. Associating the focus for a window with a document manager causes the TSF manager to automatically call <a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-setfocus">ITfThreadMgr::SetFocus</a> with the associated document manager when the associated window receives the focus.

This method can only associate a single window with a single document manager. If the implementation associates multiple document managers with a single window, or the opposite, the implementation must call <b>ITfThreadMgr::SetFocus</b> to set the focus to the proper document manager.

To restore the previous focus association, call this method with the same window handle and the value returned in the original call <i>ppdimPrev</i> for <i>pdimNew</i>. The following is an example.


```cpp

//associate the focus for m_hwnd with m_pDocMgr 
pThreadMgr->AssociateFocus(m_hwnd, m_pDocMgr, &m_pPrevDocMgr);



//Restore the original focus association. 
ITfDocumentMgr *pTempDocMgr = NULL;

pThreadMgr->AssociateFocus(m_hwnd, m_pPrevDocMgr, &pTempDocMgr);

if(pTempDocMgr)
{
    pTempDocMgr->Release();
}
    
if(m_pPrevDocMgr)
{
    m_pPrevDocMgr->Release();
}

```

## -see-also

<a href="/windows/desktop/api/msctf/nn-msctf-itfdocumentmgr">ITfDocumentMgr
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-setfocus">ITfThreadMgr::SetFocus
      </a>