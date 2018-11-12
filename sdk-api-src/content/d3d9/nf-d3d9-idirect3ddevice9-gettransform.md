---
UID: NF:d3d9.IDirect3DDevice9.GetTransform
title: IDirect3DDevice9::GetTransform
author: windows-sdk-content
description: Retrieves a matrix describing a transformation state.
old-location: direct3d9\idirect3ddevice9__gettransform.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__gettransform.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetTransform, GetTransform method [Direct3D 9], GetTransform method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetTransform method, IDirect3DDevice9.GetTransform, IDirect3DDevice9::GetTransform, a6b5ae1d-9cec-460e-5acb-c2e1bd7566e6, d3d9helper/IDirect3DDevice9::GetTransform, direct3d9.idirect3ddevice9__gettransform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IDirect3DDevice9.GetTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::GetTransform


## -description


Retrieves a matrix describing a transformation state.


## -parameters




### -param State [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172619(v=VS.85).aspx">D3DTRANSFORMSTATETYPE</a></b>

Device state variable that is being modified. This parameter can be any member of the <a href="https://msdn.microsoft.com/en-us/library/Bb172619(v=VS.85).aspx">D3DTRANSFORMSTATETYPE</a> enumerated type, or the <a href="https://msdn.microsoft.com/en-us/library/Bb172623(v=VS.85).aspx">D3DTS_WORLDMATRIX</a> macro. 


### -param pMatrix [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172573(v=VS.85).aspx">D3DMATRIX</a>*</b>

Pointer to a 
    <a href="https://msdn.microsoft.com/en-us/library/Bb172573(v=VS.85).aspx">D3DMATRIX</a> structure, describing the returned transformation state. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL if one of the arguments is invalid.




## -remarks



This method will not return device state for a device that is created using D3DCREATE_PUREDEVICE. If you want to use this method, you must create your device with any of the other flag values in <a href="https://msdn.microsoft.com/en-us/library/Bb172527(v=VS.85).aspx">D3DCREATE</a>.
    





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174463(v=VS.85).aspx">IDirect3DDevice9::SetTransform</a>
 

 

