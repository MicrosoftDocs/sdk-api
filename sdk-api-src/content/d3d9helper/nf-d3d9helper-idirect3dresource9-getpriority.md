---
UID: NF:d3d9helper.IDirect3DResource9.GetPriority
title: IDirect3DResource9::GetPriority (d3d9helper.h)
description: The IDirect3DResource9::GetPriority method (d3d9helper.h) retrieves the priority for this resource.
helpviewer_keywords: ["47c2760d-e108-6181-ef30-aa9368caa9c3","GetPriority","GetPriority method [Direct3D 9]","GetPriority method [Direct3D 9]","IDirect3DResource9 interface","IDirect3DResource9 interface [Direct3D 9]","GetPriority method","IDirect3DResource9.GetPriority","IDirect3DResource9::GetPriority","d3d9helper/IDirect3DResource9::GetPriority","direct3d9.idirect3dresource9__getpriority"]
old-location: direct3d9\idirect3dresource9__getpriority.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dresource9__getpriority.htm
ms.date: 08/11/2022
ms.keywords: 47c2760d-e108-6181-ef30-aa9368caa9c3, GetPriority, GetPriority method [Direct3D 9], GetPriority method [Direct3D 9],IDirect3DResource9 interface, IDirect3DResource9 interface [Direct3D 9],GetPriority method, IDirect3DResource9.GetPriority, IDirect3DResource9::GetPriority, d3d9helper/IDirect3DResource9::GetPriority, direct3d9.idirect3dresource9__getpriority
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DResource9::GetPriority
 - d3d9helper/IDirect3DResource9::GetPriority
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
 - IDirect3DResource9.GetPriority
---

# IDirect3DResource9::GetPriority


## -description

Retrieves the priority for this resource.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Returns a DWORD value, indicating the priority of the resource.

## -remarks

<b>IDirect3DResource9::GetPriority</b> is used for priority control of managed resources. This method returns 0 on nonmanaged resources.

Priorities are used to determine when managed resources are to be removed from memory. A resource assigned a low priority is removed before a resource with a high priority. If two resources have the same priority, the resource that was used more recently is kept in memory; the other resource is removed. Managed resources have a default priority of 0.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a>
