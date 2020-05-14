---
UID: NF:d3d9.IDirect3DVolume9.GetDevice
title: IDirect3DVolume9::GetDevice (d3d9.h)
description: Retrieves the device associated with a volume.helpviewer_keywords: ["5da9af5e-dec3-9d5d-d8ca-6c45db664c38","GetDevice","GetDevice method [Direct3D 9]","GetDevice method [Direct3D 9]","IDirect3DVolume9 interface","IDirect3DVolume9 interface [Direct3D 9]","GetDevice method","IDirect3DVolume9.GetDevice","IDirect3DVolume9::GetDevice","d3d9helper/IDirect3DVolume9::GetDevice","direct3d9.idirect3dvolume9__getdevice"]
old-location: direct3d9\idirect3dvolume9__getdevice.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvolume9__getdevice.htm
ms.date: 12/05/2018
ms.keywords: 5da9af5e-dec3-9d5d-d8ca-6c45db664c38, GetDevice, GetDevice method [Direct3D 9], GetDevice method [Direct3D 9],IDirect3DVolume9 interface, IDirect3DVolume9 interface [Direct3D 9],GetDevice method, IDirect3DVolume9.GetDevice, IDirect3DVolume9::GetDevice, d3d9helper/IDirect3DVolume9::GetDevice, direct3d9.idirect3dvolume9__getdevice
f1_keywords:
- d3d9/IDirect3DVolume9.GetDevice
dev_langs:
- c++
req.header: d3d9.h
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
- IDirect3DVolume9.GetDevice
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirect3DVolume9::GetDevice


## -description


Retrieves the device associated with a volume.


## -parameters




### -param ppDevice [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>**</b>

Address of a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a> interface to fill with the device pointer, if the query succeeds. 


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



This method allows navigation to the owning device object. 

Calling this method will increase the internal reference count on the <a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a> interface. Failure to call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> when finished using this <b>IDirect3DDevice9</b> interface results in a memory leak.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvolume9">IDirect3DVolume9</a>
 

 

