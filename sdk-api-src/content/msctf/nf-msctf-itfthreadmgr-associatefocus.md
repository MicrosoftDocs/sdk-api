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

# ITfThreadMgr::AssociateFocus


## -description




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



This method is provided as a convenience to the application developer. Associating the focus for a window with a document manager causes the TSF manager to automatically call <a href="https://msdn.microsoft.com/b437c646-2a15-4ad6-8e7e-3553e7106249">ITfThreadMgr::SetFocus</a> with the associated document manager when the associated window receives the focus.

This method can only associate a single window with a single document manager. If the implementation associates multiple document managers with a single window, or the opposite, the implementation must call <b>ITfThreadMgr::SetFocus</b> to set the focus to the proper document manager.

To restore the previous focus association, call this method with the same window handle and the value returned in the original call <i>ppdimPrev</i> for <i>pdimNew</i>. The following is an example.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
//associate the focus for m_hwnd with m_pDocMgr 
pThreadMgr-&gt;AssociateFocus(m_hwnd, m_pDocMgr, &amp;m_pPrevDocMgr);



//Restore the original focus association. 
ITfDocumentMgr *pTempDocMgr = NULL;

pThreadMgr-&gt;AssociateFocus(m_hwnd, m_pPrevDocMgr, &amp;pTempDocMgr);

if(pTempDocMgr)
{
    pTempDocMgr-&gt;Release();
}
    
if(m_pPrevDocMgr)
{
    m_pPrevDocMgr-&gt;Release();
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e99e9bdb-6a3a-438d-8fac-92ef96c8dfdd">
        ITfDocumentMgr
      </a>



<a href="https://msdn.microsoft.com/3a2ba59c-3565-4f54-ac10-923dcb4882cb">ITfThreadMgr</a>



<a href="https://msdn.microsoft.com/b437c646-2a15-4ad6-8e7e-3553e7106249">ITfThreadMgr::SetFocus
      </a>
 

 

