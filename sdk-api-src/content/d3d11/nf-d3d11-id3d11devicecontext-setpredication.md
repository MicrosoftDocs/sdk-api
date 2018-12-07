---
UID: NF:d3d11.ID3D11DeviceContext.SetPredication
title: ID3D11DeviceContext::SetPredication
author: windows-sdk-content
description: Set a rendering predicate.
old-location: direct3d11\id3d11devicecontext_setpredication.htm
tech.root: direct3d11
ms.assetid: ceac248a-31c9-4e14-892f-f047e288daae
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 98e79ffd-cbd6-1ca3-db07-4eea5d48cf38, ID3D11DeviceContext interface [Direct3D 11],SetPredication method, ID3D11DeviceContext.SetPredication, ID3D11DeviceContext::SetPredication, SetPredication, SetPredication method [Direct3D 11], SetPredication method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::SetPredication, direct3d11.id3d11devicecontext_setpredication
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.SetPredication
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext::SetPredication


## -description


Set a rendering predicate.


## -parameters




### -param pPredicate [in, optional]

Type: <b><a href="https://msdn.microsoft.com/ad16e0ac-a5ff-41ae-9b73-e93235ef891b">ID3D11Predicate</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/ad16e0ac-a5ff-41ae-9b73-e93235ef891b">ID3D11Predicate</a> interface that represents the rendering predicate. A <b>NULL</b> value indicates "no" predication; in this case, the value of <i>PredicateValue</i> is irrelevant but will be preserved for <a href="https://msdn.microsoft.com/en-us/library/Ff476429(v=VS.85).aspx">ID3D11DeviceContext::GetPredication</a>.


### -param PredicateValue [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BOOL</a></b>

If <b>TRUE</b>, rendering will be affected by when the predicate's conditions are met. If <b>FALSE</b>, rendering will be affected when the conditions are not met.


## -returns



Returns nothing.




## -remarks



The predicate must be in the "issued" or "signaled" state to be used for predication. While the predicate is set for predication, calls to <a href="https://msdn.microsoft.com/en-us/library/Ff476386(v=VS.85).aspx">ID3D11DeviceContext::Begin</a> and <a href="https://msdn.microsoft.com/en-us/library/Ff476422(v=VS.85).aspx">ID3D11DeviceContext::End</a> are invalid.

Use this method to denote that subsequent rendering and resource manipulation commands are not actually performed if the resulting predicate data of the predicate is equal to the <i>PredicateValue</i>. However, some predicates are only hints, so they may not actually prevent operations from being performed. 

The primary usefulness of predication is to allow an application to issue rendering and resource manipulation commands without taking the performance hit of spinning, waiting for <a href="https://msdn.microsoft.com/en-us/library/Ff476428(v=VS.85).aspx">ID3D11DeviceContext::GetData</a> to return. So, predication can occur while <b>ID3D11DeviceContext::GetData</b> returns <b>S_FALSE</b>. Another way to think of it: an application can also use predication as a fallback, if it is possible that <b>ID3D11DeviceContext::GetData</b> returns <b>S_FALSE</b>. If <b>ID3D11DeviceContext::GetData</b> returns <b>S_OK</b>, the application can skip calling the rendering and resource manipulation commands manually with it's own application logic.

Rendering and resource manipulation commands for Direct3D 11 include these Draw, Dispatch, Copy, Update, Clear, Generate, and Resolve operations.

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476407(v=VS.85).aspx">Draw</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476408(v=VS.85).aspx">DrawAuto</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476409(v=VS.85).aspx">DrawIndexed</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476410(v=VS.85).aspx">DrawIndexedInstanced</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476411(v=VS.85).aspx">DrawIndexedInstancedIndirect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476412(v=VS.85).aspx">DrawInstanced</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476413(v=VS.85).aspx">DrawInstancedIndirect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476405(v=VS.85).aspx">Dispatch</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476406(v=VS.85).aspx">DispatchIndirect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476392(v=VS.85).aspx">CopyResource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476393(v=VS.85).aspx">CopyStructureCount</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476394(v=VS.85).aspx">CopySubresourceRegion</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh404604(v=VS.85).aspx">CopySubresourceRegion1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn280501(v=VS.85).aspx">CopyTiles</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn280500(v=VS.85).aspx">CopyTileMappings</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476486(v=VS.85).aspx">UpdateSubresource</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh446790(v=VS.85).aspx">UpdateSubresource1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn280509(v=VS.85).aspx">UpdateTiles</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dn280508(v=VS.85).aspx">UpdateTileMappings</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476388(v=VS.85).aspx">ClearRenderTargetView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476390(v=VS.85).aspx">ClearUnorderedAccessViewFloat</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476391(v=VS.85).aspx">ClearUnorderedAccessViewUint</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Hh404601(v=VS.85).aspx">ClearView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476387(v=VS.85).aspx">ClearDepthStencilView</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476426(v=VS.85).aspx">GenerateMips</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Ff476474(v=VS.85).aspx">ResolveSubresource</a>
</li>
</ul>
You can set a rendering predicate on an immediate or a deferred context. For info about immediate and deferred contexts, see <a href="https://msdn.microsoft.com/en-us/library/Ff476892(v=VS.85).aspx">Immediate and Deferred Rendering</a>. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476385(v=VS.85).aspx">ID3D11DeviceContext</a>
 

 

