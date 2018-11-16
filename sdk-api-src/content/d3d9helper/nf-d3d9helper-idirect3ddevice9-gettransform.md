---
UID: NF:d3d9helper.IDirect3DDevice9.GetTransform
title: IDirect3DDevice9::GetTransform
author: windows-sdk-content
description: Retrieves a matrix describing a transformation state.
old-location: direct3d9\idirect3ddevice9__gettransform.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__gettransform.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetTransform, GetTransform method [Direct3D 9], GetTransform method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetTransform method, IDirect3DDevice9.GetTransform, IDirect3DDevice9::GetTransform, a6b5ae1d-9cec-460e-5acb-c2e1bd7566e6, d3d9helper/IDirect3DDevice9::GetTransform, direct3d9.idirect3ddevice9__gettransform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IDirect3DDevice9.GetTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d9helper.h
: 
- IDirect3DDevice9.GetTransform
: 
---

# IDirect3DDevice9::GetTransform


## -description


Retrieves a matrix describing a transformation state.


## -parameters




### -param State [in]

Type: <b><a href="https://msdn.microsoft.com/53535d9f-246a-42cf-82a2-fb3cf6d4ebac">D3DTRANSFORMSTATETYPE</a></b>

Device state variable that is being modified. This parameter can be any member of the <a href="https://msdn.microsoft.com/53535d9f-246a-42cf-82a2-fb3cf6d4ebac">D3DTRANSFORMSTATETYPE</a> enumerated type, or the <a href="https://msdn.microsoft.com/b0a1548c-de5d-4eff-baf9-4aecb5e13443">D3DTS_WORLDMATRIX</a> macro. 


### -param pMatrix [out]

Type: <b><a href="https://msdn.microsoft.com/d6b98a32-e745-4724-b8ce-a81a3f5416f3">D3DMATRIX</a>*</b>

Pointer to a 
    <a href="https://msdn.microsoft.com/d6b98a32-e745-4724-b8ce-a81a3f5416f3">D3DMATRIX</a> structure, describing the returned transformation state. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL if one of the arguments is invalid.




## -remarks



This method will not return device state for a device that is created using D3DCREATE_PUREDEVICE. If you want to use this method, you must create your device with any of the other flag values in <a href="https://msdn.microsoft.com/91387a2d-3927-4285-a09b-9ce247e6bfdd">D3DCREATE</a>.
    





## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/1dc94280-131f-47e8-8dd7-cea43dc6e6da">IDirect3DDevice9::SetTransform</a>
 

 

