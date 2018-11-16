---
UID: NE:d3d11_3.D3D11_FENCE_FLAG
title: D3D11_FENCE_FLAG
author: windows-sdk-content
description: Specifies fence options.
old-location: direct3d11\d3d11_fence_flag.htm
tech.root: direct3d11
ms.assetid: 745B72A2-628C-477E-8534-336E73B5268A
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: D3D11_FENCE_FLAG, D3D11_FENCE_FLAG enumeration [Direct3D 11], D3D11_FENCE_FLAG_NONE, D3D11_FENCE_FLAG_SHARED, D3D11_FENCE_FLAG_SHARED_CROSS_ADAPTER, d3d11_3/D3D11_FENCE_FLAG, d3d11_3/D3D11_FENCE_FLAG_NONE, d3d11_3/D3D11_FENCE_FLAG_SHARED, d3d11_3/D3D11_FENCE_FLAG_SHARED_CROSS_ADAPTER, direct3d11.d3d11_fence_flag
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11_3.h
api_name:
 - D3D11_FENCE_FLAG
product: Windows
targetos: Windows
req.typenames: D3D11_FENCE_FLAG
req.redist: 
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



This enum is used by the <a href="https://msdn.microsoft.com/en-us/library/Mt492479(v=VS.85).aspx">ID3D11Device::CreateFence</a> method.
      




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476152(v=VS.85).aspx">Core Enumerations</a>
 

 

