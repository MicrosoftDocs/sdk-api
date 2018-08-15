---
UID: NF:strmif.IResourceManager.NotifyRelease
title: IResourceManager::NotifyRelease
author: windows-sdk-content
description: The NotifyRelease method notifies the resource manager that IResourceConsumer has released a resource.
old-location: dshow\iresourcemanager_notifyrelease.htm
old-project: DirectShow
ms.assetid: a3779a8d-fe78-4f9b-af6c-7a25e0f07a86
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IResourceManager interface [DirectShow],NotifyRelease method, IResourceManager.NotifyRelease, IResourceManager::NotifyRelease, IResourceManagerNotifyRelease, NotifyRelease, NotifyRelease method [DirectShow], NotifyRelease method [DirectShow],IResourceManager interface, dshow.iresourcemanager_notifyrelease, strmif/IResourceManager::NotifyRelease
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.redist: 
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IResourceManager.NotifyRelease
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IResourceManager::NotifyRelease


## -description



The <code>NotifyRelease</code> method notifies the resource manager that <a href="https://msdn.microsoft.com/dda2b207-dcd8-42df-95a3-d4bfbb4a7fd8">IResourceConsumer</a> has released a resource.




## -parameters




### -param idResource [in]

Resource token.


### -param pConsumer [in]

Pointer to the object releasing the resource.


### -param bStillWant [in]

Flag that specifies whether the resource is still required. Set to <b>TRUE</b> to indicate that you still want the resource when it is next available, or <b>FALSE</b> if you no longer want the resource.


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



Use this method in response to an <a href="https://msdn.microsoft.com/9f0a5830-dcaa-4020-9e78-0cbe64e13360">IResourceConsumer::ReleaseResource</a> method, or when you have finished using the resource.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8cbe908e-5675-4134-81e7-2c5c31b0ffc5">IResourceManager Interface</a>
 

 

