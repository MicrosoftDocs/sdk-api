---
UID: NF:strmif.IResourceManager.RegisterGroup
title: IResourceManager::RegisterGroup
author: windows-sdk-content
description: The RegisterGroup method registers a named resource group with the resource manager.
old-location: dshow\iresourcemanager_registergroup.htm
tech.root: DirectShow
ms.assetid: f2d3deb2-8f22-42ac-846c-2f158f347ca7
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IResourceManager interface [DirectShow],RegisterGroup method, IResourceManager.RegisterGroup, IResourceManager::RegisterGroup, IResourceManagerRegisterGroup, RegisterGroup, RegisterGroup method [DirectShow], RegisterGroup method [DirectShow],IResourceManager interface, dshow.iresourcemanager_registergroup, strmif/IResourceManager::RegisterGroup
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
 - IResourceManager.RegisterGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IResourceManager::RegisterGroup


## -description



The <code>RegisterGroup</code> method registers a named resource group with the resource manager.




## -parameters




### -param pName [in]

Named resource group.


### -param cResource [in]

Number of resources in the group.


### -param palTokens [in]

Pointer to an array of resources in the group.


### -param plToken [out]

Pointer to the returned group resource identifier.


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
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8cbe908e-5675-4134-81e7-2c5c31b0ffc5">IResourceManager Interface</a>
 

 

