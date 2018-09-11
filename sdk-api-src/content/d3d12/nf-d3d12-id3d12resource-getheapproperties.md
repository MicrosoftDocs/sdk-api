---
UID: NF:d3d12.ID3D12Resource.GetHeapProperties
title: ID3D12Resource::GetHeapProperties
author: windows-sdk-content
description: Retrieves the properties of the resource heap, for placed and committed resources.
old-location: direct3d12\id3d12resource_getheapproperties.htm
tech.root: direct3d12
ms.assetid: 7F76986D-02F1-4E5A-B9A4-CFB021B72026
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: GetHeapProperties, GetHeapProperties method, GetHeapProperties method,ID3D12Resource interface, ID3D12Resource interface,GetHeapProperties method, ID3D12Resource.GetHeapProperties, ID3D12Resource::GetHeapProperties, d3d12/ID3D12Resource::GetHeapProperties, direct3d12.id3d12resource_getheapproperties
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
 - ID3D12Resource.GetHeapProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12Resource::GetHeapProperties


## -description


Retrieves the properties of the resource heap, for placed and committed resources.
        


## -parameters




### -param pHeapProperties [out, optional]

Type: <b><a href="https://msdn.microsoft.com/0A197D3D-67F4-46BB-8578-15E05DF46067">D3D12_HEAP_PROPERTIES</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/0A197D3D-67F4-46BB-8578-15E05DF46067">D3D12_HEAP_PROPERTIES</a> structure, that on successful completion of the method will contain the resource heap properties.
          


### -param pHeapFlags [out, optional]

Type: <b><a href="https://msdn.microsoft.com/C3C1B611-714C-49DB-8034-9C9B7D6772E4">D3D12_HEAP_FLAGS</a>*</b>

Specifies a <a href="https://msdn.microsoft.com/C3C1B611-714C-49DB-8034-9C9B7D6772E4">D3D12_HEAP_FLAGS</a> variable, that on successful completion of the method will contain any miscellaneous heap flags.
          


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/en-us/library/Dn706075(v=VS.85).aspx">Direct3D 12 Return Codes</a>.
            If the resource was created as reserved, E_INVALIDARG is returned.
          




## -remarks



This method only works on placed and committed resources, not on reserved resources.
          If the resource was created as reserved, E_INVALIDARG is returned.
          The pages could be mapped to none, one, or more heaps.
        

For more information, refer to <a href="https://msdn.microsoft.com/en-us/library/Dn899198(v=VS.85).aspx">Memory Management in Direct3D 12</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn788709(v=VS.85).aspx">ID3D12Resource</a>
 

 

