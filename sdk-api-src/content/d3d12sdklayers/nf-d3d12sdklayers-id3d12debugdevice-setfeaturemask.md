---
UID: NF:d3d12sdklayers.ID3D12DebugDevice.SetFeatureMask
title: ID3D12DebugDevice::SetFeatureMask (d3d12sdklayers.h)
author: windows-sdk-content
description: Set a bit field of flags that will turn debug features on and off.
old-location: direct3d12\id3d12debugdevice_setfeaturemask.htm
tech.root: direct3d12
ms.assetid: 12232AB8-BBEA-4663-BEB2-7E296851FE5E
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D12DebugDevice interface,SetFeatureMask method, ID3D12DebugDevice.SetFeatureMask, ID3D12DebugDevice::SetFeatureMask, SetFeatureMask, SetFeatureMask method, SetFeatureMask method,ID3D12DebugDevice interface, d3d12sdklayers/ID3D12DebugDevice::SetFeatureMask, direct3d12.id3d12debugdevice_setfeaturemask
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
 - ID3D12DebugDevice.SetFeatureMask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12DebugDevice::SetFeatureMask


## -description


Set a bit field of flags that will turn debug features on and off.
        


## -parameters




### -param Mask

Type: <b><a href="https://msdn.microsoft.com/36E0A5DC-8313-4D9D-988C-21E6FFCC8730">D3D12_DEBUG_FEATURE</a></b>

Feature-mask flags, as a bitwise-OR'd combination of <a href="https://msdn.microsoft.com/36E0A5DC-8313-4D9D-988C-21E6FFCC8730">D3D12_DEBUG_FEATURE</a> enumeration constants.
            If a flag is present, that feature will be set to on; otherwise, the feature will be set to off.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
            <a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a>





## -see-also




<a href="https://msdn.microsoft.com/E4ECE63F-6738-4856-9912-93C3AAEE7E3B">GetFeatureMask</a>



<a href="https://msdn.microsoft.com/6FD77F14-E260-4DBB-8434-664DE1F6DE39">ID3D12DebugDevice</a>
 

 

