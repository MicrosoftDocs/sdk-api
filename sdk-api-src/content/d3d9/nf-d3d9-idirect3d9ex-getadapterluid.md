---
UID: NF:d3d9.IDirect3D9Ex.GetAdapterLUID
title: IDirect3D9Ex::GetAdapterLUID
author: windows-sdk-content
description: This method returns a unique identifier for the adapter that is specific to the adapter hardware. Applications can use this identifier to define robust mappings across various APIs (Direct3D 9, DXGI).
old-location: direct3d9\idirect3d9ex_getadapterluid.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3d9ex_getadapterluid.htm
ms.author: windowssdkdev
ms.date: 04/10/2018
ms.keywords: GetAdapterLUID, GetAdapterLUID method [Direct3D 9], GetAdapterLUID method [Direct3D 9],IDirect3D9Ex interface, IDirect3D9Ex interface [Direct3D 9],GetAdapterLUID method, IDirect3D9Ex.GetAdapterLUID, IDirect3D9Ex::GetAdapterLUID, d3d9/IDirect3D9Ex::GetAdapterLUID, direct3d9.idirect3d9ex_getadapterluid, f330bb92-02a0-089a-4923-b68cf9e2282b
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d9.h
req.include-header: 
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
 - IDirect3D9Ex.GetAdapterLUID
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3D9Ex::GetAdapterLUID


## -description


This method returns a unique identifier for the adapter that is specific to the adapter hardware. Applications can use this identifier to define robust mappings across various APIs (Direct3D 9, DXGI).


## -parameters




### -param Adapter [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Ordinal number denoting the display adapter from which to retrieve the LUID.


### -param pLUID [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a>*</b>

A unique identifier for the given adapter.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb174301(v=VS.85).aspx">IDirect3D9Ex</a>
 

 

