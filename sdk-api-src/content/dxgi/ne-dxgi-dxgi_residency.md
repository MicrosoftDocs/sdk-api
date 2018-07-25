---
UID: NE:dxgi.DXGI_RESIDENCY
title: DXGI_RESIDENCY
author: windows-sdk-content
description: Flags indicating the memory location of a resource.
old-location: direct3ddxgi\DXGI_RESIDENCY.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\dxgi_residency.htm
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: DXGI_RESIDENCY, DXGI_RESIDENCY enumeration [DXGI], DXGI_RESIDENCY_EVICTED_TO_DISK, DXGI_RESIDENCY_FULLY_RESIDENT, DXGI_RESIDENCY_RESIDENT_IN_SHARED_MEMORY, cfa66ca7-3d9d-67f6-1665-f4254ee73606, direct3ddxgi.DXGI_RESIDENCY, dxgi/DXGI_RESIDENCY, dxgi/DXGI_RESIDENCY_EVICTED_TO_DISK, dxgi/DXGI_RESIDENCY_FULLY_RESIDENT, dxgi/DXGI_RESIDENCY_RESIDENT_IN_SHARED_MEMORY
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: dxgi.h
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
req.typenames: DXGI_RESIDENCY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI.h
api_name:
 - DXGI_RESIDENCY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DXGI_RESIDENCY enumeration


## -description


Flags indicating the memory location of a resource.


## -enum-fields




### -field DXGI_RESIDENCY_FULLY_RESIDENT

The resource is located in video memory.


### -field DXGI_RESIDENCY_RESIDENT_IN_SHARED_MEMORY

At least some of the resource is located in CPU memory.


### -field DXGI_RESIDENCY_EVICTED_TO_DISK

At least some of the resource has been paged out to the hard drive.


## -remarks



This enum is used by <a href="https://msdn.microsoft.com/a03af142-657b-459d-abba-fdee72e77db9">QueryResourceResidency</a>.




## -see-also




<a href="https://msdn.microsoft.com/c4574c89-dee2-4841-9318-5383cf417111">DXGI Enumerations</a>
 

 

