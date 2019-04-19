---
UID: NF:d3d12sdklayers.ID3D12DebugDevice.GetFeatureMask
title: ID3D12DebugDevice::GetFeatureMask (d3d12sdklayers.h)
author: windows-sdk-content
description: Gets a bit field of flags that indicates which debug features are on or off.
old-location: direct3d12\id3d12debugdevice_getfeaturemask.htm
tech.root: direct3d12
ms.assetid: E4ECE63F-6738-4856-9912-93C3AAEE7E3B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetFeatureMask, GetFeatureMask method, GetFeatureMask method,ID3D12DebugDevice interface, ID3D12DebugDevice interface,GetFeatureMask method, ID3D12DebugDevice.GetFeatureMask, ID3D12DebugDevice::GetFeatureMask, d3d12sdklayers/ID3D12DebugDevice::GetFeatureMask, direct3d12.id3d12debugdevice_getfeaturemask
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
 - ID3D12DebugDevice.GetFeatureMask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12DebugDevice::GetFeatureMask


## -description


Gets a bit field of flags that indicates which debug features are on or off.
        


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/36E0A5DC-8313-4D9D-988C-21E6FFCC8730">D3D12_DEBUG_FEATURE</a></b>

Mask of feature-mask flags,
            as a bitwise OR'ed combination of <a href="https://msdn.microsoft.com/36E0A5DC-8313-4D9D-988C-21E6FFCC8730">D3D12_DEBUG_FEATURE</a> enumeration constants.
            If a flag is present, then that feature will be set to on, otherwise the feature will be set to off. 
          




## -see-also




<a href="https://msdn.microsoft.com/6FD77F14-E260-4DBB-8434-664DE1F6DE39">ID3D12DebugDevice</a>



<a href="https://msdn.microsoft.com/12232AB8-BBEA-4663-BEB2-7E296851FE5E">ID3D12DebugDevice::SetFeatureMask</a>
 

 

