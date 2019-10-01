---
UID: NF:d3d12.ID3D12Device5.CheckDriverMatchingIdentifier
title: ID3D12Device5::CheckDriverMatchingIdentifier (d3d12.h)
author: windows-sdk-content
description: Reports the compatibility of serialized data, such as a serialized raytracing acceleration structure resulting from a call to CopyRaytracingAccelerationStructure with mode D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_SERIALIZE, with the current device/driver.
old-location: direct3d12\id3d12device5_checkdrivermatchingidentifier.htm
tech.root: direct3d12
ms.assetid: 765714D4-5133-4CCA-A09F-EDE650B06905
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CheckDriverMatchingIdentifier, CheckDriverMatchingIdentifier method, CheckDriverMatchingIdentifier method,ID3D12Device5 interface, ID3D12Device5 interface,CheckDriverMatchingIdentifier method, ID3D12Device5.CheckDriverMatchingIdentifier, ID3D12Device5::CheckDriverMatchingIdentifier, d3d12/ID3D12Device5::CheckDriverMatchingIdentifier, direct3d12.id3d12device5_checkdrivermatchingidentifier
ms.topic: method
f1_keywords: 
 - "d3d12/ID3D12Device5.CheckDriverMatchingIdentifier"
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - ID3D12Device5.CheckDriverMatchingIdentifier
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: RS5, 19H1
---

# ID3D12Device5::CheckDriverMatchingIdentifier


## -description


Reports the compatibility of serialized data, such as a serialized raytracing acceleration structure resulting from a call to <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-copyraytracingaccelerationstructure">CopyRaytracingAccelerationStructure</a> with mode  <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_copy_mode">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_COPY_MODE_SERIALIZE</a>, with the current device/driver.


## -parameters




### -param SerializedDataType [in]

The type of the serialized data. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ne-d3d12-d3d12_serialized_data_type">D3D12_SERIALIZED_DATA_TYPE</a>.


### -param pIdentifierToCheck [in]

Identifier from the header of the serialized data to check with the driver. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_serialized_data_driver_matching_identifier">D3D12_SERIALIZED_DATA_DRIVER_MATCHING_IDENTIFIER</a>.


## -returns



The returned compatibility status. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Mt830385(v=VS.85).aspx">D3D12_DRIVER_MATCHING_IDENTIFIER_STATUS</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt847457(v=VS.85).aspx">ID3D12Device5</a>
 

 

