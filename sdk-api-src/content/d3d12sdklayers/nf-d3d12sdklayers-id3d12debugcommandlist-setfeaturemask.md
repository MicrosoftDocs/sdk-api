---
UID: NF:d3d12sdklayers.ID3D12DebugCommandList.SetFeatureMask
title: ID3D12DebugCommandList::SetFeatureMask
author: windows-sdk-content
description: Turns the debug features for a command list on or off.
old-location: direct3d12\id3d12debugcommandlist_setfeaturemask.htm
old-project: direct3d12
ms.assetid: D2273A6C-7401-44D6-A0E3-F3F2C5DBCB8B
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: ID3D12DebugCommandList interface,SetFeatureMask method, ID3D12DebugCommandList.SetFeatureMask, ID3D12DebugCommandList::SetFeatureMask, SetFeatureMask, SetFeatureMask method, SetFeatureMask method,ID3D12DebugCommandList interface, d3d12sdklayers/ID3D12DebugCommandList::SetFeatureMask, direct3d12.id3d12debugcommandlist_setfeaturemask
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d12sdklayers.h
req.include-header: 
req.redist: 
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
req.typenames: D3D12_RLDO_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12DebugCommandList.SetFeatureMask
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12DebugCommandList::SetFeatureMask


## -description


Turns the debug features for a command list on or off.


## -parameters




### -param Mask

Type: <b><a href="https://msdn.microsoft.com/36E0A5DC-8313-4D9D-988C-21E6FFCC8730">D3D12_DEBUG_FEATURE</a></b>

A combination of feature-mask flags that are combined by using a bitwise OR operation. If a flag is present, that feature will be set to on, otherwise the feature will be set to off. 




## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>. 
          




## -see-also




<a href="https://msdn.microsoft.com/EDE527F0-4091-4B03-9030-6F693FE901BE">ID3D12DebugCommandList</a>
 

 

