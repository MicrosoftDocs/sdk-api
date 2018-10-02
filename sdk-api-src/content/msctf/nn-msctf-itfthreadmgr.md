---
UID: NN:msctf.ITfThreadMgr
title: ITfThreadMgr
author: windows-sdk-content
description: The ITfThreadMgr defines the primary object implemented by the TSF manager. ITfThreadMgr is used by applications and text services to activate and deactivate text services, create document managers, and maintain the document context focus.
old-location: tsf\itfthreadmgr.htm
tech.root: TSF
ms.assetid: 3a2ba59c-3565-4f54-ac10-923dcb4882cb
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITfThreadMgr, ITfThreadMgr interface [Text Services Framework], ITfThreadMgr interface [Text Services Framework],described, _tsf_itfthreadmgr_ref, msctf/ITfThreadMgr, tsf.itfthreadmgr
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.h
api_name:
 - ITfThreadMgr
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfThreadMgr interface


## -description


The <b>ITfThreadMgr</b> defines the primary object implemented by the TSF manager. <b>ITfThreadMgr</b> is used by applications and text services to activate and deactivate text services, create document managers, and maintain the document context focus.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfThreadMgr</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfThreadMgr</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfThreadMgr</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd9058c0-55b0-4231-a336-7cea4db75c0f">Activate</a>
</td>
<td align="left" width="63%">
Activates TSF for the calling thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2e0ef4e-5254-42c3-aebf-9d46cdee7e67">AssociateFocus</a>
</td>
<td align="left" width="63%">
Associates the focus for a window with a document manager object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f90a359-61e7-46e5-9d0b-ab6fe24f3136">CreateDocumentMgr</a>
</td>
<td align="left" width="63%">
Creates a document manager object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7293fbfa-c385-4713-80b2-760e54dbf4c1">Deactivate</a>
</td>
<td align="left" width="63%">
Deactivates TSF for the calling thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b6f61fb-0ca0-4b93-ad30-d1e080b9bde1">EnumDocumentMgrs</a>
</td>
<td align="left" width="63%">
Returns an enumerator for all the document managers within the calling thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6581cd4d-75ad-4a2c-a919-8e2eed6b3939">EnumFunctionProviders</a>
</td>
<td align="left" width="63%">
Obtains an enumerator for all of the function providers registered for the calling thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd6b4566-de23-49f5-9ef1-f82626b1f140">GetFocus</a>
</td>
<td align="left" width="63%">
Returns the document manager that has the input focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b320790a-4b54-4475-97e6-e59f083cfc09">GetFunctionProvider</a>
</td>
<td align="left" width="63%">
Obtains the specified function provider object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/801e2c3a-0445-4630-83ba-55f51ef2704e">GetGlobalCompartment</a>
</td>
<td align="left" width="63%">
Obtains the global compartment manager object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa753a4d-4f78-45e0-b711-c294adbb307a">IsThreadFocus</a>
</td>
<td align="left" width="63%">
Determines if the calling thread has the TSF input focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b437c646-2a15-4ad6-8e7e-3553e7106249">SetFocus</a>
</td>
<td align="left" width="63%">
Sets the input focus to the specified document manager.

</td>
</tr>
</table> 


## -remarks



An application obtains a pointer to this interface by calling <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> with CLSID_TF_ThreadMgr as demonstrated below.

A text service receives a pointer to this interface in its <a href="https://msdn.microsoft.com/c5fd6b5c-0a78-4b5b-aad5-0c398798cf30">ITfTextInputProcessor::Activate</a> method.


#### Examples


```cpp

HRESULT hr;
ITfThreadMgr* pThreadMgr;

hr = CoCreateInstance(  CLSID_TF_ThreadMgr, 
                        NULL, 
                        CLSCTX_INPROC_SERVER, 
                        IID_ITfThreadMgr, 
                        (void**)&pThreadMgr);

```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a>



<a href="https://msdn.microsoft.com/c5fd6b5c-0a78-4b5b-aad5-0c398798cf30">ITfTextInputProcessor::Activate
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

