---
UID: NF:msctf.ITfThreadMgr.SetFocus
title: ITfThreadMgr::SetFocus method
author: windows-driver-content
description: ITfThreadMgr::SetFocus method
old-location: tsf\itfthreadmgr_setfocus.htm
old-project: TSF
ms.assetid: b437c646-2a15-4ad6-8e7e-3553e7106249
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITfThreadMgr, ITfThreadMgr interface [Text Services Framework], SetFocus method, ITfThreadMgr::SetFocus, SetFocus method [Text Services Framework], SetFocus method [Text Services Framework], ITfThreadMgr interface, SetFocus,ITfThreadMgr.SetFocus, _tsf_itfthreadmgr_setfocus_ref, msctf/ITfThreadMgr::SetFocus, tsf.itfthreadmgr_setfocus
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
-	ITfThreadMgr.SetFocus
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfThreadMgr::SetFocus method


## -description




## -parameters




### -param pdimFocus [in]

Pointer to a <a href="https://msdn.microsoft.com/e99e9bdb-6a3a-438d-8fac-92ef96c8dfdd">ITfDocumentMgr</a> interface that receives the input focus. This parameter cannot be <b>NULL</b>.


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



The application must call this method when the document window receives the input focus. If the application associates a window with a document manager using <a href="https://msdn.microsoft.com/e2e0ef4e-5254-42c3-aebf-9d46cdee7e67">ITfThreadMgr::AssociateFocus</a>, the TSF manager calls this method for the application.




## -see-also




<a href="https://msdn.microsoft.com/e99e9bdb-6a3a-438d-8fac-92ef96c8dfdd">ITfDocumentMgr
      </a>



<a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr</a>



<a href="https://msdn.microsoft.com/e2e0ef4e-5254-42c3-aebf-9d46cdee7e67">
        ITfThreadMgr::AssociateFocus
      </a>



<a href="https://msdn.microsoft.com/bd6b4566-de23-49f5-9ef1-f82626b1f140">
        ITfThreadMgr::GetFocus
      </a>
 

 

