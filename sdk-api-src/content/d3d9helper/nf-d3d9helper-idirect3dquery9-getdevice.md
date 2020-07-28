---
UID: NF:d3d9helper.IDirect3DQuery9.GetDevice
title: IDirect3DQuery9::GetDevice (d3d9helper.h)
description: Gets the device that is being queried.
helpviewer_keywords: ["8dd8379e-a2cd-b722-e3cd-771da54e3b51","GetDevice","GetDevice method [Direct3D 9]","GetDevice method [Direct3D 9]","IDirect3DQuery9 interface","IDirect3DQuery9 interface [Direct3D 9]","GetDevice method","IDirect3DQuery9.GetDevice","IDirect3DQuery9::GetDevice","d3d9helper/IDirect3DQuery9::GetDevice","direct3d9.idirect3dquery9__getdevice"]
old-location: direct3d9\idirect3dquery9__getdevice.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dquery9__getdevice.htm
ms.date: 12/05/2018
ms.keywords: 8dd8379e-a2cd-b722-e3cd-771da54e3b51, GetDevice, GetDevice method [Direct3D 9], GetDevice method [Direct3D 9],IDirect3DQuery9 interface, IDirect3DQuery9 interface [Direct3D 9],GetDevice method, IDirect3DQuery9.GetDevice, IDirect3DQuery9::GetDevice, d3d9helper/IDirect3DQuery9::GetDevice, direct3d9.idirect3dquery9__getdevice
f1_keywords:
- d3d9helper/IDirect3DQuery9.GetDevice
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3D9.lib
- D3D9.dll
api_name:
- IDirect3DQuery9.GetDevice
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DQuery9::GetDevice


## -description


Gets the device that is being queried.


## -parameters




### -param ppDevice [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>**</b>

Pointer to the device being queried. See <a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dquery9">IDirect3DQuery9</a>
 

 

