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

# ID3D11Device1 interface


## -description


The device interface represents a virtual adapter; it is used to create resources. <b>ID3D11Device1</b> adds new methods to those in <a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Device1</b> interface inherits from <a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>. <b>ID3D11Device1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11Device1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2E891104-3706-46A5-88FB-C621C95B4EFB">CreateBlendState1</a>
</td>
<td align="left" width="63%">
Creates a blend-state object that encapsulates blend state for the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">output-merger stage</a> and allows the configuration of logic operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2F7E343F-2A25-44F2-9352-5F378718D6F6">CreateDeferredContext1</a>
</td>
<td align="left" width="63%">

      Creates a deferred context, which can record command lists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8887C3F1-3EA3-4948-A019-E3CB3F3D46C6">CreateDeviceContextState</a>
</td>
<td align="left" width="63%">

        Creates a context state object that holds all Direct3D state and some Direct3D behavior.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EBA793F1-35AA-4586-9D5C-803BD58B1D95">CreateRasterizerState1</a>
</td>
<td align="left" width="63%">
Creates a rasterizer state object that informs the <a href="https://msdn.microsoft.com/efd3f819-7c63-4e1a-9923-8e7198354ec6">rasterizer stage</a> how to behave and forces the sample count while UAV rendering or rasterizing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E66CDC7E-21B5-4675-A7A1-6F94940A4C13">GetImmediateContext1</a>
</td>
<td align="left" width="63%">
Gets an immediate context, which can play back command lists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4751B49E-01DB-467B-879C-743C8B43DDA5">OpenSharedResource1</a>
</td>
<td align="left" width="63%">
Gives a device access to a shared resource that is referenced by a handle and that was created on a different device. You must have previously created the resource as shared and specified that it uses NT handles (that is, you set the <a href="d3d11_resource_misc_flag.htm">D3D11_RESOURCE_MISC_SHARED_NTHANDLE</a> flag).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5A7575E4-382E-4A2F-AFE8-2E5850526E75">OpenSharedResourceByName</a>
</td>
<td align="left" width="63%">
Gives a device access to a shared resource that is referenced by name and that was created on a different device. You must have previously created the resource as shared and specified that it uses NT handles (that is, you set the <a href="d3d11_resource_misc_flag.htm">D3D11_RESOURCE_MISC_SHARED_NTHANDLE</a> flag).

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e96804db-0987-49ca-b1b1-321f36c13024">Core Interfaces</a>



<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 

