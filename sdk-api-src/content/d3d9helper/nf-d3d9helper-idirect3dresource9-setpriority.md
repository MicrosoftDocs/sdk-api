---
UID: NF:d3d9helper.IDirect3DResource9.SetPriority
title: IDirect3DResource9::SetPriority (d3d9helper.h)
description: The IDirect3DResource9::SetPriority method (d3d9helper.h) assigns the priority of a resource for scheduling purposes.
helpviewer_keywords: ["04209b19-79e0-1e86-73f2-4225b9102296","IDirect3DResource9 interface [Direct3D 9]","SetPriority method","IDirect3DResource9.SetPriority","IDirect3DResource9::SetPriority","SetPriority","SetPriority method [Direct3D 9]","SetPriority method [Direct3D 9]","IDirect3DResource9 interface","d3d9helper/IDirect3DResource9::SetPriority","direct3d9.idirect3dresource9__setpriority"]
old-location: direct3d9\idirect3dresource9__setpriority.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dresource9__setpriority.htm
ms.date: 08/11/2022
ms.keywords: 04209b19-79e0-1e86-73f2-4225b9102296, IDirect3DResource9 interface [Direct3D 9],SetPriority method, IDirect3DResource9.SetPriority, IDirect3DResource9::SetPriority, SetPriority, SetPriority method [Direct3D 9], SetPriority method [Direct3D 9],IDirect3DResource9 interface, d3d9helper/IDirect3DResource9::SetPriority, direct3d9.idirect3dresource9__setpriority
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
 - IDirect3DResource9::SetPriority
 - d3d9helper/IDirect3DResource9::SetPriority
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
 - IDirect3DResource9.SetPriority
---

# IDirect3DResource9::SetPriority


## -description

Assigns the priority of a resource for scheduling purposes.

## -parameters

### -param PriorityNew [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Priority to assign to a resource.
        


<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 9 for Windows Vista

The priority can be any DWORD value; Direct3D 9 for Windows Vista also supports any of these pre-defined values <a href="/windows/desktop/direct3d9/d3d9-resource-priority">D3D9_RESOURCE_PRIORITY</a>.

</td>
</tr>
</table>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Returns the previous priority value for the resource.

## -remarks

This method is used to change the priority of managed resources (resources created with the <a href="/windows/desktop/direct3d9/d3dpool">D3DPOOL_MANAGED</a> flag). This method returns 0 on non-managed resources.

Priorities are used to determine when managed resources are to be removed from memory. A resource assigned a low priority is removed before a resource with a high priority. If two resources have the same priority, the resource that was used more recently is kept in memory; the other resource is removed. Managed resources have a default priority of 0.

Windows Vista only - When this method is called using an <a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex">IDirect3D9Ex</a> interface, only resources created with the <a href="/windows/desktop/direct3d9/d3dpool">D3DPOOL_DEFAULT</a> flag will be affected.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dresource9">IDirect3DResource9</a>
