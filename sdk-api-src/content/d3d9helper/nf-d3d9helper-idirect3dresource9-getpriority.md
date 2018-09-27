---
UID: NF:d3d9helper.IDirect3DResource9.GetPriority
title: IDirect3DResource9::GetPriority
author: windows-sdk-content
description: Retrieves the priority for this resource.
old-location: direct3d9\idirect3dresource9__getpriority.htm
tech.root: Direct3D9
ms.assetid: VS|directx_sdk|~\idirect3dresource9__getpriority.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: 47c2760d-e108-6181-ef30-aa9368caa9c3, GetPriority, GetPriority method [Direct3D 9], GetPriority method [Direct3D 9],IDirect3DResource9 interface, IDirect3DResource9 interface [Direct3D 9],GetPriority method, IDirect3DResource9.GetPriority, IDirect3DResource9::GetPriority, d3d9helper/IDirect3DResource9::GetPriority, direct3d9.idirect3dresource9__getpriority
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
 - IDirect3DResource9.GetPriority
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DResource9::GetPriority


## -description


Retrieves the priority for this resource.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Returns a DWORD value, indicating the priority of the resource.




## -remarks



<b>IDirect3DResource9::GetPriority</b> is used for priority control of managed resources. This method returns 0 on nonmanaged resources.

Priorities are used to determine when managed resources are to be removed from memory. A resource assigned a low priority is removed before a resource with a high priority. If two resources have the same priority, the resource that was used more recently is kept in memory; the other resource is removed. Managed resources have a default priority of 0.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205878(v=VS.85).aspx">IDirect3DResource9</a>
 

 

