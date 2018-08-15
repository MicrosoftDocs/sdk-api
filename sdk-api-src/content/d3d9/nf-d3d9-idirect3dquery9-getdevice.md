---
UID: NF:d3d9.IDirect3DQuery9.GetDevice
title: IDirect3DQuery9::GetDevice
author: windows-sdk-content
description: Gets the device that is being queried.
old-location: direct3d9\idirect3dquery9__getdevice.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dquery9__getdevice.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 8dd8379e-a2cd-b722-e3cd-771da54e3b51, GetDevice, GetDevice method [Direct3D 9], GetDevice method [Direct3D 9],IDirect3DQuery9 interface, IDirect3DQuery9 interface [Direct3D 9],GetDevice method, IDirect3DQuery9.GetDevice, IDirect3DQuery9::GetDevice, d3d9helper/IDirect3DQuery9::GetDevice, direct3d9.idirect3dquery9__getdevice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9.h
req.include-header: D3D9.h
req.redist: 
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
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DQuery9.GetDevice
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DQuery9::GetDevice


## -description


Gets the device that is being queried.


## -parameters




### -param ppDevice






#### - pDevice [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>**</b>

Pointer to the device being queried. See <a href="https://msdn.microsoft.com/en-us/library/Bb174336(v=VS.85).aspx">IDirect3DDevice9</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205872(v=VS.85).aspx">IDirect3DQuery9</a>
 

 

