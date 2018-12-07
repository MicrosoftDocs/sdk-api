---
UID: NE:d3d11.D3D11_CPU_ACCESS_FLAG
title: D3D11_CPU_ACCESS_FLAG
author: windows-sdk-content
description: Specifies the types of CPU access allowed for a resource.
old-location: direct3d11\d3d11_cpu_access_flag.htm
tech.root: direct3d11
ms.assetid: 0a19c2a7-2570-40e2-8328-cbf5d7263605
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D11_CPU_ACCESS_FLAG, D3D11_CPU_ACCESS_FLAG enumeration [Direct3D 11], D3D11_CPU_ACCESS_READ, D3D11_CPU_ACCESS_WRITE, d3d11/D3D11_CPU_ACCESS_FLAG, d3d11/D3D11_CPU_ACCESS_READ, d3d11/D3D11_CPU_ACCESS_WRITE, direct3d11.d3d11_cpu_access_flag, e0f1ea8e-63f7-ef8a-fa11-3cbc160d2469
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3d11.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_CPU_ACCESS_FLAG
product: Windows
targetos: Windows
req.typenames: D3D11_CPU_ACCESS_FLAG
req.redist: 
---

# D3D11_CPU_ACCESS_FLAG enumeration


## -description


Specifies the types of CPU access allowed for a resource.


## -enum-fields




### -field D3D11_CPU_ACCESS_WRITE

The resource is to be mappable so that the CPU can change its contents. Resources created with this flag cannot be set as outputs of the pipeline and must be created with either dynamic or staging usage (see <a href="https://msdn.microsoft.com/251d462e-964e-42db-8554-dba8f5a9b1ef">D3D11_USAGE</a>).


### -field D3D11_CPU_ACCESS_READ

The resource is to be mappable so that the CPU can read its contents. Resources created with this flag cannot be set as either inputs or outputs to the pipeline and must be created with staging usage (see <a href="https://msdn.microsoft.com/251d462e-964e-42db-8554-dba8f5a9b1ef">D3D11_USAGE</a>).


## -remarks



This enumeration is used in <a href="https://msdn.microsoft.com/a5e470bb-011b-4a2a-96d6-cbf76fe12638">D3D11_BUFFER_DESC</a>, <a href="https://msdn.microsoft.com/8523d7b1-856e-4ec8-9286-4f1f2730a428">D3D11_TEXTURE1D_DESC</a>, <a href="https://msdn.microsoft.com/90c0f877-daf5-4b3d-9846-5bb414c55461">D3D11_TEXTURE2D_DESC</a>, <a href="https://msdn.microsoft.com/b3fd4280-c967-4eed-8a10-97f0c7ef56ac">D3D11_TEXTURE3D_DESC</a>. 

Applications may combine one or more of these flags with a logical OR. When possible, create resources with no CPU access flags, as this enables better resource optimization.

The <a href="https://msdn.microsoft.com/2a324055-21b0-4dad-a8e0-781905329dc2">D3D11_RESOURCE_MISC_FLAG</a> cannot be used when creating resources with <b>D3D11_CPU_ACCESS</b> flags.




## -see-also




<a href="https://msdn.microsoft.com/b547819b-7006-40b5-84a4-adf198048051">Resource Enumerations</a>
 

 

