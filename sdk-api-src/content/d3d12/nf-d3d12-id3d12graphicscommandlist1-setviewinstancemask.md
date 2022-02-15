---
UID: NF:d3d12.ID3D12GraphicsCommandList1.SetViewInstanceMask
title: ID3D12GraphicsCommandList1::SetViewInstanceMask (d3d12.h)
description: Set a mask that controls which view instances are enabled for subsequent draws.
helpviewer_keywords: ["ID3D12GraphicsCommandList1 interface","SetViewInstanceMask method","ID3D12GraphicsCommandList1.SetViewInstanceMask","ID3D12GraphicsCommandList1::SetViewInstanceMask","SetViewInstanceMask","SetViewInstanceMask method","SetViewInstanceMask method","ID3D12GraphicsCommandList1 interface","d3d12/ID3D12GraphicsCommandList1::SetViewInstanceMask","direct3d12.id3d12graphicscommandlist1_setviewinstancemask_uint"]
old-location: direct3d12\id3d12graphicscommandlist1_setviewinstancemask_uint.htm
tech.root: direct3d12
ms.assetid: 0AE16797-6F9E-4387-A810-EF59DDC771E6
ms.date: 12/05/2018
ms.keywords: ID3D12GraphicsCommandList1 interface,SetViewInstanceMask method, ID3D12GraphicsCommandList1.SetViewInstanceMask, ID3D12GraphicsCommandList1::SetViewInstanceMask, SetViewInstanceMask, SetViewInstanceMask method, SetViewInstanceMask method,ID3D12GraphicsCommandList1 interface, d3d12/ID3D12GraphicsCommandList1::SetViewInstanceMask, direct3d12.id3d12graphicscommandlist1_setviewinstancemask_uint
req.header: d3d12.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12GraphicsCommandList1::SetViewInstanceMask
 - d3d12/ID3D12GraphicsCommandList1::SetViewInstanceMask
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.h
api_name:
 - ID3D12GraphicsCommandList1.SetViewInstanceMask
---

# ID3D12GraphicsCommandList1::SetViewInstanceMask


## -description

Set a mask that controls which view instances are enabled for subsequent draws.

## -parameters

### -param Mask [in]

Type: <b>UINT</b>

A mask that specifies which views are enabled or disabled. If bit <i>i</i> starting from the least-significant bit is set, view instance <i>i</i> is enabled.

## -remarks

The view instance mask only affects PSOs that declare view instance masking by specifying the D3D12_VIEW_INSTANCING_FLAG_ENABLE_VIEW_INSTANCE_MASKING flag during their creation. Attempting to create a PSO that declares view instance masking will fail on adapters that don't support view instancing.

The view instance mask defaults to 0 which disables all views. This forces applications that declare view instance masking to explicitly choose the views to enable, otherwise nothing will be rendered. If the view instance mask enabled all views by default the application might not remember to disable unused views, resulting in lost performance due to wasted work.

Bundles don't inherit their view instance mask from their caller, defaulting to 0 instead. This is because the mask setting must be known when the bundle is recorded if it affects how an implementation records draws. The view instance mask set by a bundle does persist to the caller after the bundle completes, however. These inheritance semantics are similar to those of PSOs.

No shader code paths that are dependent on SV_ViewID are executed at any shader stage for view instances that are masked off and no clipping, viewport processing, or rasterization is performed. Implementations that inspect the mask during rendering can incur a small performance penalty over PSOs that don't declare view instance masking at all, but usually the penalty can be overcome by the performance savings that result from skipping the work associated with the masked off views. Depending on the frequency and amount of skipped work, the performance gains can be significant.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist1">ID3D12GraphicsCommandList1</a>