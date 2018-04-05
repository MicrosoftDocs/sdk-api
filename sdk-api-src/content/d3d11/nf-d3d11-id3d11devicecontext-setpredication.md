---
UID: NF:d3d11.ID3D11DeviceContext.SetPredication
title: ID3D11DeviceContext::SetPredication method
author: windows-driver-content
description: Set a rendering predicate.
old-location: direct3d11\id3d11devicecontext_setpredication.htm
old-project: direct3d11
ms.assetid: ceac248a-31c9-4e14-892f-f047e288daae
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: 98e79ffd-cbd6-1ca3-db07-4eea5d48cf38, ID3D11DeviceContext, ID3D11DeviceContext interface [Direct3D 11], SetPredication method, ID3D11DeviceContext::SetPredication, SetPredication method [Direct3D 11], SetPredication method [Direct3D 11], ID3D11DeviceContext interface, SetPredication,ID3D11DeviceContext.SetPredication, d3d11/ID3D11DeviceContext::SetPredication, direct3d11.id3d11devicecontext_setpredication
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
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
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11DeviceContext.SetPredication
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::SetPredication method


## -description


Set a rendering predicate.


## -parameters




### -param pPredicate [in, optional]

Type: <b><a href="https://msdn.microsoft.com/ad16e0ac-a5ff-41ae-9b73-e93235ef891b">ID3D11Predicate</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/ad16e0ac-a5ff-41ae-9b73-e93235ef891b">ID3D11Predicate</a> interface that represents the rendering predicate. A <b>NULL</b> value indicates "no" predication; in this case, the value of <i>PredicateValue</i> is irrelevant but will be preserved for <a href="https://msdn.microsoft.com/9a283895-51c4-4de5-bdeb-994f3085bd79">ID3D11DeviceContext::GetPredication</a>.


### -param PredicateValue [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

If <b>TRUE</b>, rendering will be affected by when the predicate's conditions are met. If <b>FALSE</b>, rendering will be affected when the conditions are not met.


## -returns



Returns nothing.




## -remarks



The predicate must be in the "issued" or "signaled" state to be used for predication. While the predicate is set for predication, calls to <a href="https://msdn.microsoft.com/5a9cdc60-2226-4d18-bfbd-5db10de35e53">ID3D11DeviceContext::Begin</a> and <a href="https://msdn.microsoft.com/9b941abc-04a3-4dd7-b72d-62cd5bd06b47">ID3D11DeviceContext::End</a> are invalid.

Use this method to denote that subsequent rendering and resource manipulation commands are not actually performed if the resulting predicate data of the predicate is equal to the <i>PredicateValue</i>. However, some predicates are only hints, so they may not actually prevent operations from being performed. 

The primary usefulness of predication is to allow an application to issue rendering and resource manipulation commands without taking the performance hit of spinning, waiting for <a href="https://msdn.microsoft.com/338d02ad-2227-49e5-9b4f-fb86a3898f73">ID3D11DeviceContext::GetData</a> to return. So, predication can occur while <b>ID3D11DeviceContext::GetData</b> returns <b>S_FALSE</b>. Another way to think of it: an application can also use predication as a fallback, if it is possible that <b>ID3D11DeviceContext::GetData</b> returns <b>S_FALSE</b>. If <b>ID3D11DeviceContext::GetData</b> returns <b>S_OK</b>, the application can skip calling the rendering and resource manipulation commands manually with it's own application logic.

Rendering and resource manipulation commands for Direct3D 11 include these Draw, Dispatch, Copy, Update, Clear, Generate, and Resolve operations.

<ul>
<li>
<a href="https://msdn.microsoft.com/9c63067b-c7ac-412c-ad49-c35d4fba1d68">Draw</a>
</li>
<li>
<a href="https://msdn.microsoft.com/34688e87-514f-4f85-b56b-e0245400a5ac">DrawAuto</a>
</li>
<li>
<a href="https://msdn.microsoft.com/461a64ec-f3e6-4f6a-8bc4-a349d19501a8">DrawIndexed</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c7a4821a-324c-47e4-b89f-603d2afcfb51">DrawIndexedInstanced</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c6969210-b452-4a49-a3d7-d849b1d2ebb5">DrawIndexedInstancedIndirect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3cb608e7-d64d-42cc-9b34-5f6c30af2ada">DrawInstanced</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f40c662d-7cdc-4592-b8d5-72aad0b4dd53">DrawInstancedIndirect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7d3401bb-521f-4ab0-8833-e5caf712d0c9">Dispatch</a>
</li>
<li>
<a href="https://msdn.microsoft.com/bb8840f5-ae4b-42d6-b51d-6844d0b18074">DispatchIndirect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/54c1c08a-792c-463d-8237-9f7947d15396">CopyResource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d4f8576f-8d23-4b45-a5ea-099c71e8567e">CopyStructureCount</a>
</li>
<li>
<a href="https://msdn.microsoft.com/aed89483-9870-445d-96e3-a9cee764f0ad">CopySubresourceRegion</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1963011F-C3E2-428D-B667-195A4976510B">CopySubresourceRegion1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/C336B0C7-DB99-466C-B689-5D6634EE0B36">CopyTiles</a>
</li>
<li>
<a href="https://msdn.microsoft.com/03EBF4F5-CEC3-485D-8124-AAB90DA4D6E1">CopyTileMappings</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2d8ef5a2-204a-434d-918a-104419050233">UpdateSubresource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7D89591C-F3F7-4A4F-A91A-AC67D9A573AF">UpdateSubresource1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/EB0F9CBD-29B2-484D-8923-6686C73487F7">UpdateTiles</a>
</li>
<li>
<a href="https://msdn.microsoft.com/542735C4-BFDE-4EA9-9595-BA30BD06422B">UpdateTileMappings</a>
</li>
<li>
<a href="https://msdn.microsoft.com/bbc6d3fb-b64f-47b0-9feb-a248dce0bf4b">ClearRenderTargetView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c93d8638-c624-402a-8e14-c85aa7b69930">ClearUnorderedAccessViewFloat</a>
</li>
<li>
<a href="https://msdn.microsoft.com/73e70330-63cb-4ba6-b6e5-fc9707fb9f31">ClearUnorderedAccessViewUint</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7CC8DEB6-075C-40EB-822D-8A627E285FA2">ClearView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1e2269cf-edef-466e-be59-95dc644c7a0c">ClearDepthStencilView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/43012c58-3b1a-4956-993f-4ff3f5ec7fce">GenerateMips</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7b4d6180-e3bf-475a-9865-592cda6e9f4a">ResolveSubresource</a>
</li>
</ul>
You can set a rendering predicate on an immediate or a deferred context. For info about immediate and deferred contexts, see <a href="https://msdn.microsoft.com/8991be9f-c882-4752-9048-704fe4ae1725">Immediate and Deferred Rendering</a>. 




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

