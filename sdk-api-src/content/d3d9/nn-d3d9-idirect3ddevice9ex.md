---
UID: NN:d3d9.IDirect3DDevice9Ex
title: IDirect3DDevice9Ex (d3d9.h)
description: Applications use the methods of the IDirect3DDevice9Ex interface to render primitives, create resources, work with system-level variables, adjust gamma ramp levels, work with palettes, and create shaders.
helpviewer_keywords: ["6755c62f-1ee8-9783-0c97-7e582de29a4b","IDirect3DDevice9Ex","IDirect3DDevice9Ex interface [Direct3D 9]","IDirect3DDevice9Ex interface [Direct3D 9]","described","d3d9/IDirect3DDevice9Ex","direct3d9.idirect3ddevice9ex"]
old-location: direct3d9\idirect3ddevice9ex.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex.htm
ms.date: 12/05/2018
ms.keywords: 6755c62f-1ee8-9783-0c97-7e582de29a4b, IDirect3DDevice9Ex, IDirect3DDevice9Ex interface [Direct3D 9], IDirect3DDevice9Ex interface [Direct3D 9],described, d3d9/IDirect3DDevice9Ex, direct3d9.idirect3ddevice9ex
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
 - IDirect3DDevice9Ex
 - d3d9/IDirect3DDevice9Ex
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
 - IDirect3DDevice9Ex
---

# IDirect3DDevice9Ex interface


## -description

Applications use the methods of the IDirect3DDevice9Ex interface to render primitives, create resources, work with system-level variables, adjust gamma ramp levels, work with palettes, and create shaders. The IDirect3DDevice9Ex interface derives from the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a> interface.

## -inheritance

The <b>IDirect3DDevice9Ex</b> interface inherits from <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>. <b>IDirect3DDevice9Ex</b> also has these types of members:

## -remarks

The <b>IDirect3DDevice9Ex</b> interface is obtained by calling <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex">IDirect3D9Ex::CreateDeviceEx</a>.

The LPDIRECT3DDEVICE9EX and PDIRECT3DDEVICE9EX types are defined as pointers to the IDirect3DDevice9Ex interface:



```

typedef struct IDirect3DDevice9Ex *LPDIRECT3DDEVICE9EX, *PDIRECT3DDEVICE9EX;

```




<h3><a id="Creating_a_Device"></a><a id="creating_a_device"></a><a id="CREATING_A_DEVICE"></a>Creating a Device</h3>
Follow these two steps to initialize a Direct3D device:

<ol>
<li>Call <a href="/windows/desktop/api/d3d9/nf-d3d9-direct3dcreate9ex">Direct3DCreate9Ex</a> to create the Direct3D object.</li>
<li>Call <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex">CreateDeviceEx</a> to create the Direct3D device.</li>
</ol>
Here is an example:



```

IDirect3D9Ex *pDirect3DEx;
LPDIRECT3DDEVICE9EX pDeviceEx;
DWORD behaviorFlags = D3DCREATE_HARDWARE_VERTEXPROCESSING;

Direct3DCreate9Ex(D3D_SDK_VERSION, &pDirect3DEx);
pDirect3DEx->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd, behaviorFlags, &d3dpp, NULL, &pDeviceEx);

```

## -see-also

<a href="/windows/desktop/direct3d9/dx9-graphics-reference-d3d-interfaces">Direct3D Interfaces</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
