---
UID: NF:dxgi1_2.IDXGISwapChain1.GetRotation
title: IDXGISwapChain1::GetRotation (dxgi1_2.h)
description: Gets the rotation of the back buffers for the swap chain.
helpviewer_keywords: ["GetRotation","GetRotation method [DXGI]","GetRotation method [DXGI]","IDXGISwapChain1 interface","IDXGISwapChain1 interface [DXGI]","GetRotation method","IDXGISwapChain1.GetRotation","IDXGISwapChain1::GetRotation","direct3ddxgi.idxgiswapchain1_getrotation","dxgi1_2/IDXGISwapChain1::GetRotation"]
old-location: direct3ddxgi\idxgiswapchain1_getrotation.htm
tech.root: direct3ddxgi
ms.assetid: B4460AF4-20B1-493D-88E4-2ADB304D6D60
ms.date: 12/05/2018
ms.keywords: GetRotation, GetRotation method [DXGI], GetRotation method [DXGI],IDXGISwapChain1 interface, IDXGISwapChain1 interface [DXGI],GetRotation method, IDXGISwapChain1.GetRotation, IDXGISwapChain1::GetRotation, direct3ddxgi.idxgiswapchain1_getrotation, dxgi1_2/IDXGISwapChain1::GetRotation
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
 - IDXGISwapChain1::GetRotation
 - dxgi1_2/IDXGISwapChain1::GetRotation
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
 - IDXGISwapChain1.GetRotation
---

# IDXGISwapChain1::GetRotation


## -description

Gets the rotation of the back buffers for the swap chain.

## -parameters

### -param pRotation [out]

A pointer to a variable that receives a <a href="/previous-versions/windows/desktop/legacy/bb173065(v=vs.85)">DXGI_MODE_ROTATION</a>-typed value that specifies the rotation of the back buffers for the swap chain.

## -returns

Returns S_OK if successful; an error code otherwise.  For a list of error codes, see <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="https://support.microsoft.com/help/2670838">Platform Update for Windows 7</a> installed, <b>GetRotation</b> fails with DXGI_ERROR_INVALID_CALL. For more info about the Platform Update for Windows 7, see <a href="/windows/desktop/direct3darticles/platform-update-for-windows-7">Platform Update for Windows 7</a>.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1">IDXGISwapChain1</a>