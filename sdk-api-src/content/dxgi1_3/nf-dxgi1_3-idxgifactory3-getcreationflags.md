---
UID: NF:dxgi1_3.IDXGIFactory3.GetCreationFlags
title: IDXGIFactory3::GetCreationFlags (dxgi1_3.h)
description: Gets the flags that were used when a Microsoft DirectX Graphics Infrastructure (DXGI) object was created.
helpviewer_keywords: ["GetCreationFlags","GetCreationFlags method [DXGI]","GetCreationFlags method [DXGI]","IDXGIFactory3 interface","IDXGIFactory3 interface [DXGI]","GetCreationFlags method","IDXGIFactory3.GetCreationFlags","IDXGIFactory3::GetCreationFlags","direct3ddxgi.idxgifactory3_getcreationflags","dxgi1_3/IDXGIFactory3::GetCreationFlags"]
old-location: direct3ddxgi\idxgifactory3_getcreationflags.htm
tech.root: direct3ddxgi
ms.assetid: 1B4A5DC9-6853-4047-B64D-BD251352AC89
ms.date: 12/05/2018
ms.keywords: GetCreationFlags, GetCreationFlags method [DXGI], GetCreationFlags method [DXGI],IDXGIFactory3 interface, IDXGIFactory3 interface [DXGI],GetCreationFlags method, IDXGIFactory3.GetCreationFlags, IDXGIFactory3::GetCreationFlags, direct3ddxgi.idxgifactory3_getcreationflags, dxgi1_3/IDXGIFactory3::GetCreationFlags
req.header: dxgi1_3.h
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
 - IDXGIFactory3::GetCreationFlags
 - dxgi1_3/IDXGIFactory3::GetCreationFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi1_3.h
api_name:
 - IDXGIFactory3.GetCreationFlags
---

# IDXGIFactory3::GetCreationFlags


## -description

Gets the flags that were used when a Microsoft DirectX Graphics Infrastructure (DXGI) object was created.



## -returns

The creation flags.

## -remarks

The <b>GetCreationFlags</b> method returns flags that were passed to the  <a href="/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2">CreateDXGIFactory2</a> function, or were implicitly constructed by <a href="/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory">CreateDXGIFactory</a>, <a href="/windows/desktop/api/dxgi/nf-dxgi-createdxgifactory1">CreateDXGIFactory1</a>,  <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice">D3D11CreateDevice</a>, or <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain">D3D11CreateDeviceAndSwapChain</a>.

## -see-also

<a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgifactory3">IDXGIFactory3</a>
