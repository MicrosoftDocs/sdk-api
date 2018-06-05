---
UID: NS:d3d12.D3D12_BUFFER_RTV
title: D3D12_BUFFER_RTV
author: windows-sdk-content
description: Describes the elements in a buffer resource to use in a render-target view.
old-location: direct3d12\d3d12_buffer_rtv.htm
old-project: direct3d12
ms.assetid: B4BDA7DE-6FB1-4806-9207-42EA0BFC69AE
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: D3D12_BUFFER_RTV, D3D12_BUFFER_RTV structure, d3d12/D3D12_BUFFER_RTV, direct3d12.d3d12_buffer_rtv
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d12.h
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
req.typenames: D3D12_BUFFER_RTV
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3D12.h
api_name:
-	D3D12_BUFFER_RTV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_BUFFER_RTV structure


## -description


Describes the elements in a buffer resource to use in a render-target view.


## -struct-fields




### -field FirstElement

Number of bytes between the beginning of the buffer and the first element to access.


### -field NumElements

The total number of elements in the view.


## -remarks



Use this structure with a <a href="https://msdn.microsoft.com/D8602EB9-70EB-4A4E-8D8D-A2016335AAC6">D3D12_RENDER_TARGET_VIEW_DESC</a> structure to view the resource as a buffer.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

