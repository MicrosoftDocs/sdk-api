---
UID: NF:d3d11.ID3D11DeviceContext.SetPredication
title: ID3D11DeviceContext::SetPredication (d3d11.h)
description: Set a rendering predicate. (ID3D11DeviceContext.SetPredication)
helpviewer_keywords: ["98e79ffd-cbd6-1ca3-db07-4eea5d48cf38","ID3D11DeviceContext interface [Direct3D 11]","SetPredication method","ID3D11DeviceContext.SetPredication","ID3D11DeviceContext::SetPredication","SetPredication","SetPredication method [Direct3D 11]","SetPredication method [Direct3D 11]","ID3D11DeviceContext interface","d3d11/ID3D11DeviceContext::SetPredication","direct3d11.id3d11devicecontext_setpredication"]
old-location: direct3d11\id3d11devicecontext_setpredication.htm
tech.root: direct3d11
ms.assetid: ceac248a-31c9-4e14-892f-f047e288daae
ms.date: 12/05/2018
ms.keywords: 98e79ffd-cbd6-1ca3-db07-4eea5d48cf38, ID3D11DeviceContext interface [Direct3D 11],SetPredication method, ID3D11DeviceContext.SetPredication, ID3D11DeviceContext::SetPredication, SetPredication, SetPredication method [Direct3D 11], SetPredication method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::SetPredication, direct3d11.id3d11devicecontext_setpredication
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext::SetPredication
 - d3d11/ID3D11DeviceContext::SetPredication
dev_langs:
 - c++
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
---

# ID3D11DeviceContext::SetPredication


## -description

Set a rendering predicate.

## -parameters

### -param pPredicate [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate">ID3D11Predicate</a>*</b>

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11predicate">ID3D11Predicate</a> interface that represents the rendering predicate. A <b>NULL</b> value indicates "no" predication; in this case, the value of <i>PredicateValue</i> is irrelevant but will be preserved for <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getpredication">ID3D11DeviceContext::GetPredication</a>.

### -param PredicateValue [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

If <b>TRUE</b>, rendering will be affected by when the predicate's conditions are met. If <b>FALSE</b>, rendering will be affected when the conditions are not met.

## -remarks

The predicate must be in the "issued" or "signaled" state to be used for predication. While the predicate is set for predication, calls to <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-begin">ID3D11DeviceContext::Begin</a> and <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-end">ID3D11DeviceContext::End</a> are invalid.

Use this method to denote that subsequent rendering and resource manipulation commands are not actually performed if the resulting predicate data of the predicate is equal to the <i>PredicateValue</i>. However, some predicates are only hints, so they may not actually prevent operations from being performed. 

The primary usefulness of predication is to allow an application to issue rendering and resource manipulation commands without taking the performance hit of spinning, waiting for <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-getdata">ID3D11DeviceContext::GetData</a> to return. So, predication can occur while <b>ID3D11DeviceContext::GetData</b> returns <b>S_FALSE</b>. Another way to think of it: an application can also use predication as a fallback, if it is possible that <b>ID3D11DeviceContext::GetData</b> returns <b>S_FALSE</b>. If <b>ID3D11DeviceContext::GetData</b> returns <b>S_OK</b>, the application can skip calling the rendering and resource manipulation commands manually with its own application logic.

Rendering and resource manipulation commands for Direct3D 11 include these Draw, Dispatch, Copy, Update, Clear, Generate, and Resolve operations.

<ul>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-draw">Draw</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawauto">DrawAuto</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed">DrawIndexed</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexedinstanced">DrawIndexedInstanced</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexedinstancedindirect">DrawIndexedInstancedIndirect</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawinstanced">DrawInstanced</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawinstancedindirect">DrawInstancedIndirect</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch">Dispatch</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatchindirect">DispatchIndirect</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copyresource">CopyResource</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount">CopyStructureCount</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion">CopySubresourceRegion</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1">CopySubresourceRegion1</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-copytiles">CopyTiles</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings">CopyTileMappings</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource">UpdateSubresource</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1">UpdateSubresource1</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles">UpdateTiles</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings">UpdateTileMappings</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearrendertargetview">ClearRenderTargetView</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearunorderedaccessviewfloat">ClearUnorderedAccessViewFloat</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearunorderedaccessviewuint">ClearUnorderedAccessViewUint</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-clearview">ClearView</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-cleardepthstencilview">ClearDepthStencilView</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-generatemips">GenerateMips</a>
</li>
<li>
<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-resolvesubresource">ResolveSubresource</a>
</li>
</ul>
You can set a rendering predicate on an immediate or a deferred context. For info about immediate and deferred contexts, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-render">Immediate and Deferred Rendering</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
