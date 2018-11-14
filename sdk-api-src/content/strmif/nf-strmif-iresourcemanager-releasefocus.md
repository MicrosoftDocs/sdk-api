---
UID: NF:strmif.IResourceManager.ReleaseFocus
title: IResourceManager::ReleaseFocus
author: windows-sdk-content
description: The ReleaseFocus method sets the focus object to NULL in the resource manager if the current focus object is the one specified in this method.
old-location: dshow\iresourcemanager_releasefocus.htm
tech.root: DirectShow
ms.assetid: dfc1b178-eb81-488b-8a4a-f1a454b3d5f4
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IResourceManager interface [DirectShow],ReleaseFocus method, IResourceManager.ReleaseFocus, IResourceManager::ReleaseFocus, IResourceManagerReleaseFocus, ReleaseFocus, ReleaseFocus method [DirectShow], ReleaseFocus method [DirectShow],IResourceManager interface, dshow.iresourcemanager_releasefocus, strmif/IResourceManager::ReleaseFocus
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
 - IResourceManager.ReleaseFocus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IResourceManager.ReleaseFocus
: 
---

# IResourceManager::ReleaseFocus


## -description



The <code>ReleaseFocus</code> method sets the focus object to <b>NULL</b> in the resource manager if the current focus object is the one specified in this method.




## -parameters




### -param pFocusObject [in]

Pointer to the focus object.


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



Use this method when the object of focus is about to be destroyed to ensure that the focus is not still being referenced.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8cbe908e-5675-4134-81e7-2c5c31b0ffc5">IResourceManager Interface</a>
 

 

