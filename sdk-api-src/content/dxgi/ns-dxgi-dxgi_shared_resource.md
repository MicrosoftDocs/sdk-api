---
UID: NS:dxgi.DXGI_SHARED_RESOURCE
title: DXGI_SHARED_RESOURCE
author: windows-sdk-content
description: Represents a handle to a shared resource.
old-location: direct3ddxgi\dxgi_shared_resource.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\dxgi_shared_resource.htm
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: DXGI_SHARED_RESOURCE, DXGI_SHARED_RESOURCE structure [DXGI], aa3179a5-6a16-4e5d-df66-783c4edeb8f4, direct3ddxgi.dxgi_shared_resource, dxgi/DXGI_SHARED_RESOURCE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI.h
api_name:
 - DXGI_SHARED_RESOURCE
product: Windows
targetos: Windows
req.typenames: DXGI_SHARED_RESOURCE
req.redist: 
---

# DXGI_SHARED_RESOURCE structure


## -description


Represents a handle to a shared resource.


## -struct-fields




### -field Handle

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HANDLE</a></b>

A handle to a shared resource.


## -remarks



To create a shared surface, pass a shared-resource handle into the <a href="https://msdn.microsoft.com/d0effc0a-0ec9-4350-ac44-c64c29984a02">IDXGIDevice::CreateSurface</a> method.




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>
 

 

