---
UID: NF:d3d12sdklayers.ID3D12DebugDevice.SetFeatureMask
title: ID3D12DebugDevice::SetFeatureMask
author: windows-sdk-content
description: Set a bit field of flags that will turn debug features on and off.
old-location: direct3d12\id3d12debugdevice_setfeaturemask.htm
tech.root: direct3d12
ms.assetid: 12232AB8-BBEA-4663-BEB2-7E296851FE5E
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: ID3D12DebugDevice interface,SetFeatureMask method, ID3D12DebugDevice.SetFeatureMask, ID3D12DebugDevice::SetFeatureMask, SetFeatureMask, SetFeatureMask method, SetFeatureMask method,ID3D12DebugDevice interface, d3d12sdklayers/ID3D12DebugDevice::SetFeatureMask, direct3d12.id3d12debugdevice_setfeaturemask
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
 - ID3D12DebugDevice.SetFeatureMask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d12sdklayers.h
: 
- ID3D12DebugDevice.SetFeatureMask
: 
---

# ID3D12DebugDevice::SetFeatureMask


## -description


Set a bit field of flags that will turn debug features on and off.
        


## -parameters




### -param Mask

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dn950141(v=VS.85).aspx">D3D12_DEBUG_FEATURE</a></b>

Feature-mask flags, as a bitwise-OR'd combination of <a href="https://msdn.microsoft.com/en-us/library/Dn950141(v=VS.85).aspx">D3D12_DEBUG_FEATURE</a> enumeration constants.
            If a flag is present, that feature will be set to on; otherwise, the feature will be set to off.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/en-us/library/Dn706075(v=VS.85).aspx">Direct3D 12 Return Codes</a>.
            <a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn986874(v=VS.85).aspx">GetFeatureMask</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn986873(v=VS.85).aspx">ID3D12DebugDevice</a>
 

 

