---
UID: NF:msctf.ITfThreadMgr.GetFocus
title: ITfThreadMgr::GetFocus
author: windows-driver-content
description: ITfThreadMgr::GetFocus method
old-location: tsf\itfthreadmgr_getfocus.htm
old-project: TSF
ms.assetid: bd6b4566-de23-49f5-9ef1-f82626b1f140
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: GetFocus, GetFocus method [Text Services Framework], GetFocus method [Text Services Framework],ITfThreadMgr interface, ITfThreadMgr interface [Text Services Framework],GetFocus method, ITfThreadMgr.GetFocus, ITfThreadMgr::GetFocus, _tsf_itfthreadmgr_getfocus_ref, msctf/ITfThreadMgr::GetFocus, tsf.itfthreadmgr_getfocus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfThreadMgr.GetFocus
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfThreadMgr::GetFocus


## -description




## -parameters




### -param ppdimFocus [out]

Pointer to a <a href="https://msdn.microsoft.com/e99e9bdb-6a3a-438d-8fac-92ef96c8dfdd">ITfDocumentMgr</a> interface that receives the document manager with the current input focus. Receives <b>NULL</b> if no document manager has the focus.


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




<a href="https://msdn.microsoft.com/e99e9bdb-6a3a-438d-8fac-92ef96c8dfdd">ITfDocumentMgr
      </a>



<a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr</a>



<a href="https://msdn.microsoft.com/e2e0ef4e-5254-42c3-aebf-9d46cdee7e67">
        ITfThreadMgr::AssociateFocus
      </a>



<a href="https://msdn.microsoft.com/b437c646-2a15-4ad6-8e7e-3553e7106249">
        ITfThreadMgr::SetFocus
      </a>
 

 

