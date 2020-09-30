---
UID: NF:d3d9.IDirect3DDevice9Ex.WaitForVBlank
title: IDirect3DDevice9Ex::WaitForVBlank (d3d9.h)
description: Suspend execution of the calling thread until the next vertical blank signal.
helpviewer_keywords: ["0c60116d-ada5-3625-26f3-44646e467dd6","IDirect3DDevice9Ex interface [Direct3D 9]","WaitForVBlank method","IDirect3DDevice9Ex.WaitForVBlank","IDirect3DDevice9Ex::WaitForVBlank","WaitForVBlank","WaitForVBlank method [Direct3D 9]","WaitForVBlank method [Direct3D 9]","IDirect3DDevice9Ex interface","d3d9/IDirect3DDevice9Ex::WaitForVBlank","direct3d9.idirect3ddevice9ex_waitforvblank"]
old-location: direct3d9\idirect3ddevice9ex_waitforvblank.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex_waitforvblank.htm
ms.date: 12/05/2018
ms.keywords: 0c60116d-ada5-3625-26f3-44646e467dd6, IDirect3DDevice9Ex interface [Direct3D 9],WaitForVBlank method, IDirect3DDevice9Ex.WaitForVBlank, IDirect3DDevice9Ex::WaitForVBlank, WaitForVBlank, WaitForVBlank method [Direct3D 9], WaitForVBlank method [Direct3D 9],IDirect3DDevice9Ex interface, d3d9/IDirect3DDevice9Ex::WaitForVBlank, direct3d9.idirect3ddevice9ex_waitforvblank
req.header: d3d9.h
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DDevice9Ex::WaitForVBlank
 - d3d9/IDirect3DDevice9Ex::WaitForVBlank
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9Ex.WaitForVBlank
---

# IDirect3DDevice9Ex::WaitForVBlank


## -description

Suspend execution of the calling thread until the next vertical blank signal.

## -parameters

### -param iSwapChain [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Swap chain index. This is an optional, zero-based index used to specify a swap chain on a multihead card.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method will always return D3D_OK.

## -remarks

This method allows applications to efficiently throttle their frame rate to that of the monitor associated with the device. Following a vertical blank, the amount of time it takes for the thread to wake up is typically very short.

In some scenarios the hardware may stop generating vertical blank signals when nothing is being displayed on the monitor. In this case, the method will wait approximately 100ms and return with D3D_OK.

## -see-also

<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex">IDirect3DDevice9Ex</a>