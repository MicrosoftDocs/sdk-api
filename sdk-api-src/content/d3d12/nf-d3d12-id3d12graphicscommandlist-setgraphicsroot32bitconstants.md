---
UID: NF:d3d12.ID3D12GraphicsCommandList.SetGraphicsRoot32BitConstants
title: ID3D12GraphicsCommandList::SetGraphicsRoot32BitConstants
author: windows-sdk-content
description: Sets a group of constants in the graphics root signature.
old-location: direct3d12\id3d12graphicscommandlist_setgraphicsroot32bitconstants.htm
tech.root: direct3d12
ms.assetid: 509B8AA0-8128-4216-A9E2-67C027488E4A
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D12GraphicsCommandList interface,SetGraphicsRoot32BitConstants method, ID3D12GraphicsCommandList.SetGraphicsRoot32BitConstants, ID3D12GraphicsCommandList::SetGraphicsRoot32BitConstants, SetGraphicsRoot32BitConstants, SetGraphicsRoot32BitConstants method, SetGraphicsRoot32BitConstants method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::SetGraphicsRoot32BitConstants, direct3d12.id3d12graphicscommandlist_setgraphicsroot32bitconstants
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList.SetGraphicsRoot32BitConstants
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12GraphicsCommandList::SetGraphicsRoot32BitConstants


## -description


Sets a group of constants in the graphics root signature.
        


## -parameters




### -param RootParameterIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The slot number for binding.
          


### -param Num32BitValuesToSet [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of constants to set in the root signature.
          


### -param pSrcData [in]

Type: <b>const void*</b>

The source data for the group of constants to set.
          


### -param DestOffsetIn32BitValues [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The offset, in 32-bit values, to set the first constant of the group in the root signature.
          


## -returns



This method does not return a value.
          




## -see-also




<a href="https://msdn.microsoft.com/1BF282A7-F6D4-43A9-BDAD-D877564A1C6B">ID3D12GraphicsCommandList</a>
 

 

