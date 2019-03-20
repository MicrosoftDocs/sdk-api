---
UID: NF:d3d9helper.IDirect3DDevice9.GetStreamSourceFreq
title: IDirect3DDevice9::GetStreamSourceFreq (d3d9helper.h)
author: windows-sdk-content
description: Gets the stream source frequency divider value.
old-location: direct3d9\idirect3ddevice9__getstreamsourcefreq.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getstreamsourcefreq.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 5a7d1b69-c1ef-f38d-2536-b01c718bd9b6, GetStreamSourceFreq, GetStreamSourceFreq method [Direct3D 9], GetStreamSourceFreq method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetStreamSourceFreq method, IDirect3DDevice9.GetStreamSourceFreq, IDirect3DDevice9::GetStreamSourceFreq, d3d9helper/IDirect3DDevice9::GetStreamSourceFreq, direct3d9.idirect3ddevice9__getstreamsourcefreq
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
 - IDirect3DDevice9.GetStreamSourceFreq
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::GetStreamSourceFreq


## -description


Gets the stream source frequency divider value.


## -parameters




### -param StreamNumber [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Stream source number.


#### - Divider [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Returns the frequency divider value.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



Vertex shaders can now be invoked more than once per vertex. See <a href="https://msdn.microsoft.com/en-us/library/Bb173349(v=VS.85).aspx">Drawing Non-Indexed Geometry</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174460(v=VS.85).aspx">IDirect3DDevice9::SetStreamSourceFreq</a>
 

 

