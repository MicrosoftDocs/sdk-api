---
UID: NF:d3d9.IDirect3DResource9.PreLoad
title: IDirect3DResource9::PreLoad
author: windows-sdk-content
description: Preloads a managed resource.
old-location: direct3d9\idirect3dresource9__preload.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dresource9__preload.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IDirect3DResource9 interface [Direct3D 9],PreLoad method, IDirect3DResource9.PreLoad, IDirect3DResource9::PreLoad, PreLoad, PreLoad method [Direct3D 9], PreLoad method [Direct3D 9],IDirect3DResource9 interface, d3d9helper/IDirect3DResource9::PreLoad, direct3d9.idirect3dresource9__preload, eae2783a-4a7c-f994-50b0-b5b5c735921f
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IDirect3DResource9.PreLoad
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DResource9::PreLoad


## -description


Preloads a managed resource.


## -parameters






## -returns



This method does not return a value.




## -remarks



Calling this method indicates that the application will need this managed resource shortly. This method has no effect on nonmanaged resources.

<b>IDirect3DResource9::PreLoad</b> detects "thrashing" conditions where more resources are being used in each frame than can fit in video memory simultaneously. Under such circumstances <b>IDirect3DResource9::PreLoad</b> silently does nothing.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205878(v=VS.85).aspx">IDirect3DResource9</a>
 

 

