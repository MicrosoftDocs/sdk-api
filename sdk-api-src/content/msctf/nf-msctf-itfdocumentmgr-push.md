---
UID: NF:msctf.ITfDocumentMgr.Push
title: ITfDocumentMgr::Push method
author: windows-driver-content
description: ITfDocumentMgr::Push method
old-location: tsf\itfdocumentmgr_push.htm
old-project: TSF
ms.assetid: afd5452b-4121-428d-801f-1638c2767c67
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ITfDocumentMgr, ITfDocumentMgr interface [Text Services Framework], Push method, ITfDocumentMgr::Push, Push method [Text Services Framework], Push method [Text Services Framework], ITfDocumentMgr interface, Push,ITfDocumentMgr.Push, _tsf_itfdocumentmgr_push_ref, msctf/ITfDocumentMgr::Push, tsf.itfdocumentmgr_push
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
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
-	msctf.dll
api_name:
-	ITfDocumentMgr.Push
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfDocumentMgr::Push method


## -description




## -parameters




### -param pic [in]

Pointer to the <a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext</a> object to be added to the stack. This object is obtained from a previous call to <a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">ITfDocumentMgr::CreateContext</a>.


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
<i>pic</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_STACKFULL</b></dt>
</dl>
</td>
<td width="60%">
No space exists on the stack for the context. The context stack has a limit of two contexts.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
This method was called during an <a href="https://msdn.microsoft.com/bbf65d8d-5a59-4c4b-a132-fa28babcd70b">ITfDocumentMgr::Pop</a> call.

</td>
</tr>
</table>
 




## -remarks



The first context added to the stack becomes the main document context.

The TSF manager and text services only interact with the context at the top of the stack. Normally, only the main document context is on the stack. Occasionally, it is necessary to add a second context to the stack. For example, when a text service must display a modal UI, such as a candidate list. During this time, the text service will add its context to the stack. When the text service UI is no longer required, the text service removes the context from the stack. The main context then returns to the top of the stack. To simplify this process and prevent multiple modal UIs from being displayed, there is a maximum of two contexts allowed on the stack.

This method causes the <a href="https://msdn.microsoft.com/80fbb861-1a12-4a9a-8f96-332c2f736f2d">ITfThreadMgrEventSink::OnPushContext</a> method of all installed thread manager event sinks to be called. If this is the first context to be added to the stack, this method causes the <a href="https://msdn.microsoft.com/18586e51-66b6-4071-88b4-9b92d5449a45">ITfThreadMgrEventSink::OnInitDocumentMgr</a> method of all installed thread manager event sinks to be called.


<a href="https://msdn.microsoft.com/bbf65d8d-5a59-4c4b-a132-fa28babcd70b">ITfDocumentMgr::Pop</a> must be called to remove this context from the context stack.




## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
      </a>



<a href="https://msdn.microsoft.com/e99e9bdb-6a3a-438d-8fac-92ef96c8dfdd">ITfDocumentMgr</a>



<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">
        ITfDocumentMgr::CreateContext
      </a>



<a href="https://msdn.microsoft.com/bbf65d8d-5a59-4c4b-a132-fa28babcd70b">
        ITfDocumentMgr::Pop
      </a>



<a href="https://msdn.microsoft.com/18586e51-66b6-4071-88b4-9b92d5449a45">
        ITfThreadMgrEventSink::OnInitDocumentMgr
      </a>



<a href="https://msdn.microsoft.com/80fbb861-1a12-4a9a-8f96-332c2f736f2d">
        ITfThreadMgrEventSink::OnPushContext
      </a>
 

 

