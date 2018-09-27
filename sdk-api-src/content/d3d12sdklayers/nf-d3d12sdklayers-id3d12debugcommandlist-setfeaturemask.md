---
UID: NF:d3d12sdklayers.ID3D12DebugCommandList.SetFeatureMask
title: ID3D12DebugCommandList::SetFeatureMask
author: windows-sdk-content
description: Turns the debug features for a command list on or off.
old-location: direct3d12\id3d12debugcommandlist_setfeaturemask.htm
tech.root: direct3d12
ms.assetid: D2273A6C-7401-44D6-A0E3-F3F2C5DBCB8B
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: ID3D12DebugCommandList interface,SetFeatureMask method, ID3D12DebugCommandList.SetFeatureMask, ID3D12DebugCommandList::SetFeatureMask, SetFeatureMask, SetFeatureMask method, SetFeatureMask method,ID3D12DebugCommandList interface, d3d12sdklayers/ID3D12DebugCommandList::SetFeatureMask, direct3d12.id3d12debugcommandlist_setfeaturemask
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d12sdklayers.h
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
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12DebugCommandList.SetFeatureMask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12DebugCommandList::SetFeatureMask


## -description


Turns the debug features for a command list on or off.


## -parameters




### -param Mask

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn950141(v=VS.85).aspx">D3D12_DEBUG_FEATURE</a></b>

A combination of feature-mask flags that are combined by using a bitwise OR operation. If a flag is present, that feature will be set to on, otherwise the feature will be set to off. 




## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/en-us/library/Dn706075(v=VS.85).aspx">Direct3D 12 Return Codes</a>. 
          




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn950154(v=VS.85).aspx">ID3D12DebugCommandList</a>
 

 

