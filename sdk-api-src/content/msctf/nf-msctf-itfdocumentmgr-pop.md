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

# ITfDocumentMgr::Pop


## -description




## -parameters




### -param dwFlags [in]

If this value is 0, only the context at the top of the stack is removed. If this value is TF_POPF_ALL, all of the contexts are removed from the stack.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The stack is empty or this method is called without the TF_POPF_ALL flag and only a single context is on the stack.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
This method was called during another <b>ITfDocumentMgr::Pop</b> call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>dwFlags</i> is invalid.

</td>
</tr>
</table>
 




## -remarks



This method must be called from the same thread as the corresponding <a href="https://msdn.microsoft.com/afd5452b-4121-428d-801f-1638c2767c67">ITfDocumentMgr::Push</a> call.

The first context added to the stack becomes the primary context. The primary context cannot be removed from the stack without using the TF_POPF_ALL flag. When the document is uninitialized, this method should be called with the TF_POPF_ALL flag. This causes the document manager to remove all contexts from the context stack and terminate any text service UI. Do not use the TF_POPF_ALL flag at any other time.

This method causes the <a href="https://msdn.microsoft.com/de07d7cf-db91-44e0-a0b2-4de26262552f">ITfThreadMgrEventSink::OnPopContext</a> method of all installed thread manager event sinks to be called. If the last context is removed from the stack, this method causes the <a href="https://msdn.microsoft.com/da4532e4-aa00-41af-8dfc-1880dc5b3b22">ITfThreadMgrEventSink::OnUninitDocumentMgr</a> method of all installed thread manager event sinks to be called.




## -see-also




<a href="https://msdn.microsoft.com/e99e9bdb-6a3a-438d-8fac-92ef96c8dfdd">ITfDocumentMgr</a>



<a href="https://msdn.microsoft.com/afd5452b-4121-428d-801f-1638c2767c67">ITfDocumentMgr::Push
      </a>



<a href="https://msdn.microsoft.com/de07d7cf-db91-44e0-a0b2-4de26262552f">
        ITfThreadMgrEventSink::OnPopContext
      </a>



<a href="https://msdn.microsoft.com/da4532e4-aa00-41af-8dfc-1880dc5b3b22">
        ITfThreadMgrEventSink::OnUninitDocumentMgr
      </a>
 

 

