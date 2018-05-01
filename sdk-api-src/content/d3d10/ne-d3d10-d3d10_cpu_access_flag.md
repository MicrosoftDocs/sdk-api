---
UID: NE:d3d10.D3D10_CPU_ACCESS_FLAG
title: D3D10_CPU_ACCESS_FLAG
author: windows-driver-content
description: Specifies the types of CPU access allowed for a resource.
old-location: direct3d10\d3d10_cpu_access_flag.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_cpu_access_flag.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: 9751a6d6-e112-7fe3-72df-bf449b5579c2, D3D10_CPU_ACCESS_FLAG, D3D10_CPU_ACCESS_FLAG enumeration [Direct3D 10], D3D10_CPU_ACCESS_READ, D3D10_CPU_ACCESS_WRITE, d3d10/D3D10_CPU_ACCESS_FLAG, d3d10/D3D10_CPU_ACCESS_READ, d3d10/D3D10_CPU_ACCESS_WRITE, direct3d10.d3d10_cpu_access_flag
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: d3d10.h
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
req.typenames: D3D10_CPU_ACCESS_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D10.h
api_name:
-	D3D10_CPU_ACCESS_FLAG
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# D3D10_CPU_ACCESS_FLAG enumeration


## -description


Specifies the types of CPU access allowed for a resource.


## -enum-fields




### -field D3D10_CPU_ACCESS_WRITE

The resource is to be <a href="https://msdn.microsoft.com/34fd4d15-ee64-4acf-967d-a4afb6f26329">mappable</a> so that the CPU can change its contents. Resources created with this flag cannot be set as outputs of the pipeline and must be created with either dynamic or staging usage (see <a href="https://msdn.microsoft.com/eaaf695c-e99d-4bf8-b479-fa2d06d53248">D3D10_USAGE</a>).


### -field D3D10_CPU_ACCESS_READ

The resource is to be <a href="https://msdn.microsoft.com/34fd4d15-ee64-4acf-967d-a4afb6f26329">mappable</a> so that the CPU can read its contents. Resources created with this flag cannot be set as either inputs or outputs to the pipeline and must be created with staging usage (see <a href="https://msdn.microsoft.com/eaaf695c-e99d-4bf8-b479-fa2d06d53248">D3D10_USAGE</a>).


## -remarks



This enumeration is used in <a href="https://msdn.microsoft.com/3f98c741-ff4c-4080-bd57-ef35cd6622d6">D3D10_BUFFER_DESC</a>, <a href="https://msdn.microsoft.com/f4230e66-5b38-4c69-8406-974fb7708c16">D3D10_TEXTURE1D_DESC</a>, <a href="https://msdn.microsoft.com/2535da35-7985-4e50-b840-6a636f871697">D3D10_TEXTURE2D_DESC</a>, <a href="https://msdn.microsoft.com/b2447872-cbef-4cf2-ab7c-2739343ceb64">D3D10_TEXTURE3D_DESC</a>, and <a href="https://msdn.microsoft.com/8325d50e-a8a9-4ee2-87e2-e60fb3699af6">D3DX10_IMAGE_LOAD_INFO</a>. See <a href="https://msdn.microsoft.com/9787b153-9301-4a0f-bd6f-21cc6f7fc650">Creating Buffer Resources (Direct3D 10)</a> for more details.

Applications can combine one or more of these flags with a bitwise OR. When possible, create resources with no CPU access flags, as this enables better resource optimization.




## -see-also




<a href="https://msdn.microsoft.com/c986b22c-2960-4571-98bc-028c9f41ec65">Resource Enumerations</a>
 

 

