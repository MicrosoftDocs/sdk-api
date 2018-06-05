---
UID: NE:d3d11_3.D3D11_FENCE_FLAG
title: D3D11_FENCE_FLAG
author: windows-sdk-content
description: Specifies fence options.
old-location: direct3d11\d3d11_fence_flag.htm
old-project: direct3d11
ms.assetid: 745B72A2-628C-477E-8534-336E73B5268A
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: D3D11_FENCE_FLAG, D3D11_FENCE_FLAG enumeration [Direct3D 11], D3D11_FENCE_FLAG_NONE, D3D11_FENCE_FLAG_SHARED, D3D11_FENCE_FLAG_SHARED_CROSS_ADAPTER, d3d11_3/D3D11_FENCE_FLAG, d3d11_3/D3D11_FENCE_FLAG_NONE, d3d11_3/D3D11_FENCE_FLAG_SHARED, d3d11_3/D3D11_FENCE_FLAG_SHARED_CROSS_ADAPTER, direct3d11.d3d11_fence_flag
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d11_3.h
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
req.typenames: D3D11_FENCE_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	d3d11_3.h
api_name:
-	D3D11_FENCE_FLAG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_FENCE_FLAG enumeration


## -description



          Specifies fence options.
        


## -enum-fields




### -field D3D11_FENCE_FLAG_NONE


            No options are specified.
          


### -field D3D11_FENCE_FLAG_SHARED


            The fence is shared.
          


### -field D3D11_FENCE_FLAG_SHARED_CROSS_ADAPTER


            The fence is shared with another GPU adapter.
          


### -field D3D11_FENCE_FLAG_NON_MONITORED




## -remarks




        This enum is used by the <a href="https://msdn.microsoft.com/B4AA9E0D-AAF4-4632-A98F-A3212764D5E1">ID3D11Device::CreateFence</a> method.
      




## -see-also




<a href="https://msdn.microsoft.com/1641713a-5ac8-4597-900b-1bba54f9f522">Core Enumerations</a>
 

 

