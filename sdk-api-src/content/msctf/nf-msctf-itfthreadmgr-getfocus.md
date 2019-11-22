---
UID: NF:msctf.ITfThreadMgr.GetFocus
title: ITfThreadMgr::GetFocus (msctf.h)

description: ITfThreadMgr::GetFocus method
old-location: tsf\itfthreadmgr_getfocus.htm
tech.root: TSF
ms.assetid: bd6b4566-de23-49f5-9ef1-f82626b1f140

ms.date: 12/05/2018
ms.keywords: GetFocus, GetFocus method [Text Services Framework], GetFocus method [Text Services Framework],ITfThreadMgr interface, ITfThreadMgr interface [Text Services Framework],GetFocus method, ITfThreadMgr.GetFocus, ITfThreadMgr::GetFocus, _tsf_itfthreadmgr_getfocus_ref, msctf/ITfThreadMgr::GetFocus, tsf.itfthreadmgr_getfocus
ms.topic: method
f1_keywords: 
 - "msctf/ITfThreadMgr.GetFocus"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfThreadMgr.GetFocus
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfThreadMgr::GetFocus


## -description




## -parameters




### -param ppdimFocus [out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfdocumentmgr">ITfDocumentMgr</a> interface that receives the document manager with the current input focus. Receives <b>NULL</b> if no document manager has the focus.


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
No document manager has focus. <i>ppdimFocus</i> be set to <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppdimFocus</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfdocumentmgr">ITfDocumentMgr
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-associatefocus">ITfThreadMgr::AssociateFocus
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-setfocus">ITfThreadMgr::SetFocus
      </a>
 

 

