---
UID: NF:d3d9helper.IDirect3DDevice9.SetStreamSourceFreq
title: IDirect3DDevice9::SetStreamSourceFreq
author: windows-sdk-content
description: Sets the stream source frequency divider value. This may be used to draw several instances of geometry.
old-location: direct3d9\idirect3ddevice9__setstreamsourcefreq.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setstreamsourcefreq.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],SetStreamSourceFreq method, IDirect3DDevice9.SetStreamSourceFreq, IDirect3DDevice9::SetStreamSourceFreq, SetStreamSourceFreq, SetStreamSourceFreq method [Direct3D 9], SetStreamSourceFreq method [Direct3D 9],IDirect3DDevice9 interface, c801693e-69ab-254b-92c2-993cfa9ec78a, d3d9helper/IDirect3DDevice9::SetStreamSourceFreq, direct3d9.idirect3ddevice9__setstreamsourcefreq
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
 - IDirect3DDevice9.SetStreamSourceFreq
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
- IDirect3DDevice9.SetStreamSourceFreq
: 
---

# IDirect3DDevice9::SetStreamSourceFreq


## -description


Sets the stream source frequency divider value. This may be used to draw several instances of geometry.


## -parameters




### -param StreamNumber [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Stream source number.


### -param Divider

TBD




#### - FrequencyParameter [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

This parameter may have two different values. See remarks.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



There are two constants defined in d3d9types.h that are designed to use with SetStreamSourceFreq: D3DSTREAMSOURCE_INDEXEDDATA and D3DSTREAMSOURCE_INSTANCEDATA. To see how to use the constants, see <a href="https://msdn.microsoft.com/en-us/library/Bb173349(v=VS.85).aspx">Efficiently Drawing Multiple Instances of Geometry (Direct3D 9)</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb174410(v=VS.85).aspx">IDirect3DDevice9::GetStreamSourceFreq</a>
 

 

