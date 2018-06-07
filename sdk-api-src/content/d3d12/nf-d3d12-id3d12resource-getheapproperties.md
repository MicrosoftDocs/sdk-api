---
UID: NF:d3d12.ID3D12Resource.GetHeapProperties
title: ID3D12Resource::GetHeapProperties
author: windows-sdk-content
description: Retrieves the properties of the resource heap, for placed and committed resources.
old-location: direct3d12\id3d12resource_getheapproperties.htm
old-project: direct3d12
ms.assetid: 7F76986D-02F1-4E5A-B9A4-CFB021B72026
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: GetHeapProperties, GetHeapProperties method, GetHeapProperties method,ID3D12Resource interface, ID3D12Resource interface,GetHeapProperties method, ID3D12Resource.GetHeapProperties, ID3D12Resource::GetHeapProperties, d3d12/ID3D12Resource::GetHeapProperties, direct3d12.id3d12resource_getheapproperties
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D_SHADER_MODEL
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
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



Type: <b><a href="https://msdn.microsoft.com/library/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


            This method returns one of the <a href="https://msdn.microsoft.com/5F6CC962-7DB7-489F-82A4-9388313014D3">Direct3D 12 Return Codes</a>.
            If the resource was created as reserved, E_INVALIDARG is returned.
          




## -remarks




          This method only works on placed and committed resources, not on reserved resources.
          If the resource was created as reserved, E_INVALIDARG is returned.
          The pages could be mapped to none, one, or more heaps.
        


          For more information, refer to <a href="https://msdn.microsoft.com/94D47EBB-8060-49F6-A1FF-8B7B98AD5363">Memory Management in Direct3D 12</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/AF453D2F-F0FD-4552-A843-84119A829CD5">ID3D12Resource</a>
 

 

