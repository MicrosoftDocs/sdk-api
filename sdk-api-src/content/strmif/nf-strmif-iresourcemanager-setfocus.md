---
UID: NF:strmif.IResourceManager.SetFocus
title: IResourceManager::SetFocus
author: windows-sdk-content
description: The SetFocus method notifies the resource manager that a specified object has been given the focus of the user.
old-location: dshow\iresourcemanager_setfocus.htm
tech.root: DirectShow
ms.assetid: 3d0a87e1-6774-45cf-9ab5-18ec1d2fff0d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IResourceManager interface [DirectShow],SetFocus method, IResourceManager.SetFocus, IResourceManager::SetFocus, IResourceManagerSetFocus, SetFocus, SetFocus method [DirectShow], SetFocus method [DirectShow],IResourceManager interface, dshow.iresourcemanager_setfocus, strmif/IResourceManager::SetFocus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IResourceManager.SetFocus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IResourceManager::SetFocus


## -description



The <code>SetFocus</code> method notifies the resource manager that a specified object has been given the focus of the user.




## -parameters




### -param pFocusObject [in]

Pointer to the object that has been given the user's focus.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation. <b>HRESULT</b> can be one of the following standard constants, or other values not listed.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method isn't supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK or NOERROR</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -remarks



In DirectShow, the object given the user's focus is typically a video renderer whose window has received the focus. The resource manager gives priority to requests for resources in the following order:

<ol>
<li>Requests made with the focus object specified in the <i>pFocusObject</i> parameter.</li>
<li>Requests whose focus object shares a common source filter.</li>
<li>Requests whose focus object shares a common filter graph.</li>
<li>Requests in the same process as the focus.</li>
</ol>
After a focus has been set, the resource manager must maintain a focus object until <a href="https://msdn.microsoft.com/dfc1b178-eb81-488b-8a4a-f1a454b3d5f4">ReleaseFocus</a> is called. That is, after calling this method, you must use <b>ReleaseFocus</b> before the <b>IUnknown</b> interface of the focus object becomes invalid, unless you can guarantee that <code>SetFocus</code> is called by a different object in the meantime. No reference count is held on the focus object.

The resource manager will hold this pointer until replaced or canceled, and will use it to resolve resource contention. It will use <b>QueryInterface</b> for the <a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter</a> interface at least and, if found, will use methods on that interface. It calls methods on <b>IBaseFilter</b> to decide which audio renderer to use if there are two (it will choose the one with a source filter common to the focus object), and also to determine if the two objects are within the same filter graph.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8cbe908e-5675-4134-81e7-2c5c31b0ffc5">IResourceManager Interface</a>
 

 

