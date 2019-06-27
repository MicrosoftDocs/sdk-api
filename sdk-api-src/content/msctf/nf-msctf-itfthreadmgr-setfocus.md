---
UID: NF:msctf.ITfThreadMgr.SetFocus
title: ITfThreadMgr::SetFocus (msctf.h)
author: windows-sdk-content
description: ITfThreadMgr::SetFocus method
old-location: tsf\itfthreadmgr_setfocus.htm
tech.root: TSF
ms.assetid: b437c646-2a15-4ad6-8e7e-3553e7106249
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfThreadMgr interface [Text Services Framework],SetFocus method, ITfThreadMgr.SetFocus, ITfThreadMgr::SetFocus, SetFocus, SetFocus method [Text Services Framework], SetFocus method [Text Services Framework],ITfThreadMgr interface, _tsf_itfthreadmgr_setfocus_ref, msctf/ITfThreadMgr::SetFocus, tsf.itfthreadmgr_setfocus
ms.topic: method
f1_keywords: 
 - "msctf/ITfThreadMgr.SetFocus"
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
 - ITfThreadMgr.SetFocus
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfThreadMgr::SetFocus


## -description




## -parameters




### -param pdimFocus [in]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfdocumentmgr">ITfDocumentMgr</a> interface that receives the input focus. This parameter cannot be <b>NULL</b>.


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
<i>pdimFocus</i> is invalid.

</td>
</tr>
</table>
 




## -remarks



The application must call this method when the document window receives the input focus. If the application associates a window with a document manager using <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-associatefocus">ITfThreadMgr::AssociateFocus</a>, the TSF manager calls this method for the application.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfdocumentmgr">ITfDocumentMgr
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-associatefocus">ITfThreadMgr::AssociateFocus
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfthreadmgr-getfocus">ITfThreadMgr::GetFocus
      </a>
 

 

