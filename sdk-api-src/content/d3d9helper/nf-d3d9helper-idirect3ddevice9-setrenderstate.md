---
UID: NF:d3d9helper.IDirect3DDevice9.SetRenderState
title: IDirect3DDevice9::SetRenderState
author: windows-sdk-content
description: Sets a single device render-state parameter.
old-location: direct3d9\idirect3ddevice9__setrenderstate.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setrenderstate.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 80316479-a08a-1e20-c73a-1d392c1204d6, IDirect3DDevice9 interface [Direct3D 9],SetRenderState method, IDirect3DDevice9.SetRenderState, IDirect3DDevice9::SetRenderState, SetRenderState, SetRenderState method [Direct3D 9], SetRenderState method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetRenderState, direct3d9.idirect3ddevice9__setrenderstate
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3DVSHADERCAPS2_0
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::SetRenderState


## -description


Sets a single device render-state parameter.


## -parameters




### -param State [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff549036">D3DRENDERSTATETYPE</a></b>

Device state variable that is being modified. This parameter can be any member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff549036">D3DRENDERSTATETYPE</a> enumerated type. 


### -param Value [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

New value for the device render state to be set. The meaning of this parameter is dependent on the value specified for <i>State</i>. For example, if <i>State</i> were D3DRS_SHADEMODE, the second parameter would be one member of the <a href="https://msdn.microsoft.com/ba4e0c62-b496-427b-a324-2fb560d153ba">D3DSHADEMODE</a> enumerated type. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if one of the arguments is invalid.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/0ec6a1fd-d310-4316-a9e6-60378320ea12">IDirect3DDevice9::GetRenderState</a>



<a href="https://msdn.microsoft.com/1dc94280-131f-47e8-8dd7-cea43dc6e6da">IDirect3DDevice9::SetTransform</a>
 

 

