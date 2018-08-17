---
UID: NF:d3d12sdklayers.ID3D12DebugDevice.GetFeatureMask
title: ID3D12DebugDevice::GetFeatureMask
author: windows-sdk-content
description: Gets a bit field of flags that indicates which debug features are on or off.
old-location: direct3d12\id3d12debugdevice_getfeaturemask.htm
old-project: direct3d12
ms.assetid: E4ECE63F-6738-4856-9912-93C3AAEE7E3B
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: GetFeatureMask, GetFeatureMask method, GetFeatureMask method,ID3D12DebugDevice interface, ID3D12DebugDevice interface,GetFeatureMask method, ID3D12DebugDevice.GetFeatureMask, ID3D12DebugDevice::GetFeatureMask, d3d12sdklayers/ID3D12DebugDevice::GetFeatureMask, direct3d12.id3d12debugdevice_getfeaturemask
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
 - ID3D12DebugDevice.GetFeatureMask
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12DebugDevice::GetFeatureMask


## -description


Gets a bit field of flags that indicates which debug features are on or off.
        


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn950141(v=VS.85).aspx">D3D12_DEBUG_FEATURE</a></b>

Mask of feature-mask flags,
            as a bitwise OR'ed combination of <a href="https://msdn.microsoft.com/en-us/library/Dn950141(v=VS.85).aspx">D3D12_DEBUG_FEATURE</a> enumeration constants.
            If a flag is present, then that feature will be set to on, otherwise the feature will be set to off. 
          




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn986873(v=VS.85).aspx">ID3D12DebugDevice</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn986876(v=VS.85).aspx">ID3D12DebugDevice::SetFeatureMask</a>
 

 

