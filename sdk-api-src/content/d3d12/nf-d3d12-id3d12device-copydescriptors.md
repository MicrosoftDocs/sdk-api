---
UID: NF:d3d12.ID3D12Device.CopyDescriptors
title: ID3D12Device::CopyDescriptors (d3d12.h)
author: windows-sdk-content
description: Copies descriptors from a source to a destination.
old-location: direct3d12\id3d12device_copydescriptors.htm
tech.root: direct3d12
ms.assetid: F995EF34-74FF-4FCA-A018-E2F48DF92450
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CopyDescriptors, CopyDescriptors method, CopyDescriptors method,ID3D12Device interface, ID3D12Device interface,CopyDescriptors method, ID3D12Device.CopyDescriptors, ID3D12Device::CopyDescriptors, d3d12/ID3D12Device::CopyDescriptors, direct3d12.id3d12device_copydescriptors
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Device.CopyDescriptors
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Device::CopyDescriptors


## -description


Copies descriptors from a source to a destination.
        


## -parameters




### -param NumDestDescriptorRanges [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of destination descriptor ranges to copy to.
          


### -param pDestDescriptorRangeStarts [in]

Type: <b>const <a href="https://msdn.microsoft.com/92451E4C-5E70-4015-8760-3F75066A44FD">D3D12_CPU_DESCRIPTOR_HANDLE</a>*</b>

An array of CPU_descriptor_handle objects to copy to.
          


### -param pDestDescriptorRangeSizes [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

An array of destination descriptor range sizes to copy to.
          


### -param NumSrcDescriptorRanges [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of source descriptor ranges to copy from.
          


### -param pSrcDescriptorRangeStarts [in]

Type: <b>const <a href="https://msdn.microsoft.com/92451E4C-5E70-4015-8760-3F75066A44FD">D3D12_CPU_DESCRIPTOR_HANDLE</a>*</b>

An array of CPU_descriptor_handle objects to copy from.
          


### -param pSrcDescriptorRangeSizes [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

An array of source descriptor range sizes to copy from.
          


### -param DescriptorHeapsType [in]

Type: <b><a href="https://msdn.microsoft.com/E74C78BC-B0FC-473A-B4F3-434F50A55E9F">D3D12_DESCRIPTOR_HEAP_TYPE</a></b>

The <a href="https://msdn.microsoft.com/E74C78BC-B0FC-473A-B4F3-434F50A55E9F">D3D12_DESCRIPTOR_HEAP_TYPE</a>-typed value that specifies the type of descriptor heap to copy with.
          


## -returns



Returns nothing.
          




## -see-also




<a href="https://msdn.microsoft.com/65AE4D96-6221-46B5-BF55-F86479FCF97C">Copying Descriptors</a>



<a href="https://msdn.microsoft.com/D32B3397-A1E0-48AF-9251-2EDA96261A9F">ID3D12Device</a>
 

 

