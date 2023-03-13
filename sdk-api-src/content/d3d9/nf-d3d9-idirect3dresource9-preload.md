---
UID: NF:d3d9.IDirect3DResource9.PreLoad
title: IDirect3DResource9::PreLoad (d3d9.h)
description: The IDirect3DResource9::PreLoad (d3d9.h) method preloads a managed resource.
helpviewer_keywords: ["IDirect3DResource9 interface [Direct3D 9]","PreLoad method","IDirect3DResource9.PreLoad","IDirect3DResource9::PreLoad","PreLoad","PreLoad method [Direct3D 9]","PreLoad method [Direct3D 9]","IDirect3DResource9 interface","d3d9helper/IDirect3DResource9::PreLoad","direct3d9.idirect3dresource9__preload","eae2783a-4a7c-f994-50b0-b5b5c735921f"]
old-location: direct3d9\idirect3dresource9__preload.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dresource9__preload.htm
ms.date: 08/11/2022
ms.keywords: IDirect3DResource9 interface [Direct3D 9],PreLoad method, IDirect3DResource9.PreLoad, IDirect3DResource9::PreLoad, PreLoad, PreLoad method [Direct3D 9], PreLoad method [Direct3D 9],IDirect3DResource9 interface, d3d9helper/IDirect3DResource9::PreLoad, direct3d9.idirect3dresource9__preload, eae2783a-4a7c-f994-50b0-b5b5c735921f
req.header: d3d9.h
req.include-header: D3d9.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DResource9::PreLoad
 - d3d9/IDirect3DResource9::PreLoad
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DResource9.PreLoad
---

# IDirect3DResource9::PreLoad


## -description

Preloads a managed resource.



## -remarks

Calling this method indicates that the application will need this managed resource shortly. This method has no effect on nonmanaged resources.

<b>IDirect3DResource9::PreLoad</b> detects "thrashing" conditions where more resources are being used in each frame than can fit in video memory simultaneously. Under such circumstances <b>IDirect3DResource9::PreLoad</b> silently does nothing.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a>
