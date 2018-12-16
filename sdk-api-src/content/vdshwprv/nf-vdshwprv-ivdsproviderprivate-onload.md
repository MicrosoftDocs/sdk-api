---
UID: NF:vdshwprv.IVdsProviderPrivate.OnLoad
title: IVdsProviderPrivate::OnLoad
author: windows-sdk-content
description: Prompts the provider to initialize itself, and passes a callback object that the provider uses to get necessary interfaces.
old-location: base\ivdsproviderprivate_onload.htm
tech.root: vds
ms.assetid: c5b2ac78-6a23-470c-a762-26ce6358e0b6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVdsProviderPrivate interface [VDS],OnLoad method, IVdsProviderPrivate.OnLoad, IVdsProviderPrivate::OnLoad, OnLoad, OnLoad method [VDS], OnLoad method [VDS],IVdsProviderPrivate interface, base.ivdsproviderprivate_onload, vdshwprv/IVdsProviderPrivate::OnLoad
ms.topic: method
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsProviderPrivate.OnLoad
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsProviderPrivate::OnLoad


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Prompts the provider to 
   initialize itself, and passes a callback object that the provider uses to get necessary interfaces.
  


## -parameters




### -param pwszMachineName [in]

This parameter is reserved.


### -param pCallbackObject [in]

Pointer to a callback object.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="https://msdn.microsoft.com/en-us/library/ms680746(v=VS.85).aspx">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The provider is initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VDS_E_INITIALIZED_FAILED</b></dt>
<dt>0x80042401L</dt>
</dl>
</td>
<td width="60%">
The provider failed to initialize.

</td>
</tr>
</table>
 




## -remarks



VDS calls this method immediately after calling the <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> method on a provider.

Implementers must implement this method. Invoke the  <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a> method 
    to query for the <a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a>



<a href="https://msdn.microsoft.com/5f1c38bf-85a7-4123-becb-e8abf3052b41">IVdsProviderPrivate</a>



<a href="https://msdn.microsoft.com/8c4b2a0b-f056-4d3f-976c-0339c930e3cf">IVdsProviderPrivate::OnUnload</a>
 

 

