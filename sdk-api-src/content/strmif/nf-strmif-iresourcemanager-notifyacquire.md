---
UID: NF:strmif.IResourceManager.NotifyAcquire
title: IResourceManager::NotifyAcquire
author: windows-sdk-content
description: The NotifyAcquire method notifies the resource manager that an attempt to acquire a resource has completed.
old-location: dshow\iresourcemanager_notifyacquire.htm
tech.root: DirectShow
ms.assetid: a5c52f5b-1c21-4f4c-b698-15b6ec7f7fed
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IResourceManager interface [DirectShow],NotifyAcquire method, IResourceManager.NotifyAcquire, IResourceManager::NotifyAcquire, IResourceManagerNotifyAcquire, NotifyAcquire, NotifyAcquire method [DirectShow], NotifyAcquire method [DirectShow],IResourceManager interface, dshow.iresourcemanager_notifyacquire, strmif/IResourceManager::NotifyAcquire
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
 - IResourceManager.NotifyAcquire
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IResourceManager::NotifyAcquire


## -description



The <code>NotifyAcquire</code> method notifies the resource manager that an attempt to acquire a resource has completed.




## -parameters




### -param idResource [in]

Token for the registered resource.


### -param pConsumer [in]

Pointer to the <a href="https://msdn.microsoft.com/dda2b207-dcd8-42df-95a3-d4bfbb4a7fd8">IResourceConsumer</a> interface of the object requesting the resource.


### -param hr [in]

Value indicating the success of the acquisition; S_OK if the resource was acquired, or an error value if not.


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



Use this method after an <a href="https://msdn.microsoft.com/e88d90af-681e-483b-9b29-9844eec75e41">IResourceConsumer::AcquireResource</a> method returns an S_FALSE value, indicating that the acquisition will be asynchronous (that is, handled by a callback mechanism). If the <i>hr</i> parameter is S_OK, the resource manager will assume that the resource is now held by the caller. If the <i>hr</i> parameter is anything other than S_OK, the resource manager will assume that the attempt to acquire the resource failed and will reassign the resource elsewhere.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8cbe908e-5675-4134-81e7-2c5c31b0ffc5">IResourceManager Interface</a>
 

 

