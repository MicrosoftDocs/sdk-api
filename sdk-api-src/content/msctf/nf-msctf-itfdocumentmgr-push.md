---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ITfDocumentMgr::Push


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
 

 

