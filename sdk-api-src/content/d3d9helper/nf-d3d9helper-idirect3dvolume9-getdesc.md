---
UID: NF:d3d9helper.IDirect3DVolume9.GetDesc
title: IDirect3DVolume9::GetDesc
author: windows-sdk-content
description: Retrieves a description of the volume.
old-location: direct3d9\idirect3dvolume9__getdesc.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dvolume9__getdesc.htm
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: 6ce3365b-f9f8-dd10-e1a5-c17ea631f175, GetDesc, GetDesc method [Direct3D 9], GetDesc method [Direct3D 9],IDirect3DVolume9 interface, IDirect3DVolume9 interface [Direct3D 9],GetDesc method, IDirect3DVolume9.GetDesc, IDirect3DVolume9::GetDesc, d3d9helper/IDirect3DVolume9::GetDesc, direct3d9.idirect3dvolume9__getdesc
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
 - IDirect3DVolume9.GetDesc
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DVolume9::GetDesc


## -description


Retrieves a description of the volume.


## -parameters




### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/library/Bb172633(v=VS.85).aspx">D3DVOLUME_DESC</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/Bb172633(v=VS.85).aspx">D3DVOLUME_DESC</a> structure, describing the volume. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if the argument is invalid.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb205932(v=VS.85).aspx">IDirect3DVolume9</a>
 

 

