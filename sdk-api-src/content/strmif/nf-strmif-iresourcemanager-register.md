---
UID: NF:strmif.IResourceManager.Register
title: IResourceManager::Register
author: windows-sdk-content
description: The Register method registers a single named resource with the resource manager.
old-location: dshow\iresourcemanager_register.htm
tech.root: DirectShow
ms.assetid: 23fa6830-144b-479f-8a8e-b637d82f51d1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IResourceManager interface [DirectShow],Register method, IResourceManager.Register, IResourceManager::Register, IResourceManagerRegister, Register, Register method [DirectShow], Register method [DirectShow],IResourceManager interface, dshow.iresourcemanager_register, strmif/IResourceManager::Register
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
 - IResourceManager.Register
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IResourceManager::Register


## -description



The <code>Register</code> method registers a single named resource with the resource manager.




## -parameters




### -param pName [in]

Named resource.


### -param cResource [in]

Number of resources.


### -param plToken [out]

Pointer to the returned token identifying the resource to be used in additional calls.


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



This method registers a named resource, which can contain a number of resources, and returns a token to be used when requesting this resource. It is not an error if the resource is already registered; if the number in the <i>cResource</i> parameter is less than what is already registered, resources will be deallocated to the new count. To unregister the resource, pass a count of zero in <i>cResource</i>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/8cbe908e-5675-4134-81e7-2c5c31b0ffc5">IResourceManager Interface</a>
 

 

