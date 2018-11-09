---
UID: NF:d3d9helper.IDirect3DDevice9.SetRenderState
title: IDirect3DDevice9::SetRenderState
author: windows-sdk-content
description: Sets a single device render-state parameter.
old-location: direct3d9\idirect3ddevice9__setrenderstate.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setrenderstate.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: 80316479-a08a-1e20-c73a-1d392c1204d6, IDirect3DDevice9 interface [Direct3D 9],SetRenderState method, IDirect3DDevice9.SetRenderState, IDirect3DDevice9::SetRenderState, SetRenderState, SetRenderState method [Direct3D 9], SetRenderState method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetRenderState, direct3d9.idirect3ddevice9__setrenderstate
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
 - IDirect3DDevice9.SetRenderState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::SetRenderState


## -description


Sets a single device render-state parameter.


## -parameters




### -param State [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172599(v=VS.85).aspx">D3DRENDERSTATETYPE</a></b>

Device state variable that is being modified. This parameter can be any member of the <a href="https://msdn.microsoft.com/en-us/library/Bb172599(v=VS.85).aspx">D3DRENDERSTATETYPE</a> enumerated type. 


### -param Value [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

New value for the device render state to be set. The meaning of this parameter is dependent on the value specified for <i>State</i>. For example, if <i>State</i> were D3DRS_SHADEMODE, the second parameter would be one member of the <a href="https://msdn.microsoft.com/en-us/library/Bb172605(v=VS.85).aspx">D3DSHADEMODE</a> enumerated type. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if one of the arguments is invalid.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174403(v=VS.85).aspx">IDirect3DDevice9::GetRenderState</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174463(v=VS.85).aspx">IDirect3DDevice9::SetTransform</a>
 

 

