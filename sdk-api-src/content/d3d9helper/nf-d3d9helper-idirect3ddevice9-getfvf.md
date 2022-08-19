---
UID: NF:d3d9helper.IDirect3DDevice9.GetFVF
title: IDirect3DDevice9::GetFVF (d3d9helper.h)
description: The IDirect3DDevice9::GetFVF method (d3d9.h) gets the fixed vertex function declaration.
helpviewer_keywords: ["951f24cf-f72e-7ab4-8fde-fbe96bc36c7a","GetFVF","GetFVF method [Direct3D 9]","GetFVF method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetFVF method","IDirect3DDevice9.GetFVF","IDirect3DDevice9::GetFVF","d3d9helper/IDirect3DDevice9::GetFVF","direct3d9.idirect3ddevice9__getfvf"]
old-location: direct3d9\idirect3ddevice9__getfvf.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getfvf.htm
ms.date: 08/11/2022
ms.keywords: 951f24cf-f72e-7ab4-8fde-fbe96bc36c7a, GetFVF, GetFVF method [Direct3D 9], GetFVF method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetFVF method, IDirect3DDevice9.GetFVF, IDirect3DDevice9::GetFVF, d3d9helper/IDirect3DDevice9::GetFVF, direct3d9.idirect3ddevice9__getfvf
req.header: d3d9helper.h
req.include-header: D3D9.h
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
 - IDirect3DDevice9::GetFVF
 - d3d9helper/IDirect3DDevice9::GetFVF
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
 - IDirect3DDevice9.GetFVF
---

# IDirect3DDevice9::GetFVF


## -description

Gets the fixed vertex function declaration.

## -parameters

### -param pFVF [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

A DWORD pointer to the fixed function vertex type. For more information, see <a href="/windows/desktop/direct3d9/d3dfvf">D3DFVF</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be
     D3DERR_INVALIDCALL.

## -remarks

The fixed vertex function declaration is a set of FVF flags that determine how vertices processed by the fixed function pipeline will be used.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setfvf">IDirect3DDevice9::SetFVF</a>
