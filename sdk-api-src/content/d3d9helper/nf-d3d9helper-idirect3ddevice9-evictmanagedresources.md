---
UID: NF:d3d9helper.IDirect3DDevice9.EvictManagedResources
title: IDirect3DDevice9::EvictManagedResources (d3d9helper.h)
description: The IDirect3DDevice9::EvictManagedResources method (d3d9.h) evicts all managed resources, including both Direct3D and driver-managed resources.
helpviewer_keywords: ["EvictManagedResources","EvictManagedResources method [Direct3D 9]","EvictManagedResources method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","EvictManagedResources method","IDirect3DDevice9.EvictManagedResources","IDirect3DDevice9::EvictManagedResources","d3d9helper/IDirect3DDevice9::EvictManagedResources","direct3d9.idirect3ddevice9__evictmanagedresources","ec2856fb-c12d-5e50-485d-460fa48f8758"]
old-location: direct3d9\idirect3ddevice9__evictmanagedresources.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__evictmanagedresources.htm
ms.date: 08/11/2022
ms.keywords: EvictManagedResources, EvictManagedResources method [Direct3D 9], EvictManagedResources method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],EvictManagedResources method, IDirect3DDevice9.EvictManagedResources, IDirect3DDevice9::EvictManagedResources, d3d9helper/IDirect3DDevice9::EvictManagedResources, direct3d9.idirect3ddevice9__evictmanagedresources, ec2856fb-c12d-5e50-485d-460fa48f8758
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
 - IDirect3DDevice9::EvictManagedResources
 - d3d9helper/IDirect3DDevice9::EvictManagedResources
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
 - IDirect3DDevice9.EvictManagedResources
---

# IDirect3DDevice9::EvictManagedResources


## -description

Evicts all managed resources, including both Direct3D and driver-managed resources.



## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_OUTOFVIDEOMEMORY, D3DERR_COMMAND_UNPARSED.

## -remarks

This function causes only the D3DPOOL_DEFAULT copy of resources to be evicted. The resource copy in system memory is retained. See <a href="/windows/desktop/direct3d9/d3dpool">D3DPOOL</a>.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
