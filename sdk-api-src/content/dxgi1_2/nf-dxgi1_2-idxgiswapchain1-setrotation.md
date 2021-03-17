---
UID: NF:dxgi1_2.IDXGISwapChain1.SetRotation
title: IDXGISwapChain1::SetRotation (dxgi1_2.h)
description: Sets the rotation of the back buffers for the swap chain.
helpviewer_keywords: ["IDXGISwapChain1 interface [DXGI]","SetRotation method","IDXGISwapChain1.SetRotation","IDXGISwapChain1::SetRotation","SetRotation","SetRotation method [DXGI]","SetRotation method [DXGI]","IDXGISwapChain1 interface","direct3ddxgi.idxgiswapchain1_setrotation","dxgi1_2/IDXGISwapChain1::SetRotation"]
old-location: direct3ddxgi\idxgiswapchain1_setrotation.htm
tech.root: direct3ddxgi
ms.assetid: D1CD2B20-FC7E-4141-A828-96E070A63F4A
ms.date: 12/05/2018
ms.keywords: IDXGISwapChain1 interface [DXGI],SetRotation method, IDXGISwapChain1.SetRotation, IDXGISwapChain1::SetRotation, SetRotation, SetRotation method [DXGI], SetRotation method [DXGI],IDXGISwapChain1 interface, direct3ddxgi.idxgiswapchain1_setrotation, dxgi1_2/IDXGISwapChain1::SetRotation
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxgi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGISwapChain1::SetRotation
 - dxgi1_2/IDXGISwapChain1::SetRotation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGISwapChain1.SetRotation
---

# IDXGISwapChain1::SetRotation


## -description

Sets the rotation of the back buffers for the swap chain.

## -parameters

### -param Rotation [in]

A <a href="/previous-versions/windows/desktop/legacy/bb173065(v=vs.85)">DXGI_MODE_ROTATION</a>-typed value that specifies how to set the rotation of the back buffers for the swap chain.

## -returns

<b>SetRotation</b> returns:
        <ul>
<li>S_OK if it successfully set the rotation.</li>
<li>DXGI_ERROR_INVALID_CALL if the swap chain is bit-block transfer (bitblt) model. The swap chain must be flip model to successfully call <b>SetRotation</b>.</li>
<li>Possibly other error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.</li>
</ul>


<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="https://support.microsoft.com/help/2670838">Platform Update for Windows 7</a> installed, <b>SetRotation</b> fails with DXGI_ERROR_INVALID_CALL. For more info about the Platform Update for Windows 7, see <a href="/windows/desktop/direct3darticles/platform-update-for-windows-7">Platform Update for Windows 7</a>.

## -remarks

You can only use <b>SetRotation</b> to rotate the back buffers for flip-model swap chains that you present in windowed mode. 

<b>SetRotation</b> isn't supported for rotating the back buffers for flip-model swap chains that you present in full-screen mode. In this situation, <b>SetRotation</b> doesn't fail, but you must ensure that you specify no rotation (<a href="/previous-versions/windows/desktop/legacy/bb173065(v=vs.85)">DXGI_MODE_ROTATION_IDENTITY</a>) for the swap chain. Otherwise, when you call <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">IDXGISwapChain1::Present1</a> or <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">IDXGISwapChain::Present</a> to present a frame,  the presentation fails.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1">IDXGISwapChain1</a>