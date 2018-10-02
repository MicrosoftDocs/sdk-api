---
UID: NF:d3d11shader.ID3D11ModuleInstance.BindResourceAsUnorderedAccessViewByName
title: ID3D11ModuleInstance::BindResourceAsUnorderedAccessViewByName
author: windows-sdk-content
description: Rebinds a resource by name as an unordered access view (UAV) to destination slots.
old-location: direct3d11\id3d11moduleinstance_bindresourceasunorderedaccessviewbyname.htm
tech.root: direct3d11
ms.assetid: B9A9BA35-7CAB-411D-8168-B126CB8C3139
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BindResourceAsUnorderedAccessViewByName, BindResourceAsUnorderedAccessViewByName method [Direct3D 11], BindResourceAsUnorderedAccessViewByName method [Direct3D 11],ID3D11ModuleInstance interface, ID3D11ModuleInstance interface [Direct3D 11],BindResourceAsUnorderedAccessViewByName method, ID3D11ModuleInstance.BindResourceAsUnorderedAccessViewByName, ID3D11ModuleInstance::BindResourceAsUnorderedAccessViewByName, d3d11shader/ID3D11ModuleInstance::BindResourceAsUnorderedAccessViewByName, direct3d11.id3d11moduleinstance_bindresourceasunorderedaccessviewbyname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11shader.h
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
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3D11ModuleInstance.BindResourceAsUnorderedAccessViewByName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11ModuleInstance::BindResourceAsUnorderedAccessViewByName


## -description


Rebinds a resource by name as an unordered access view (UAV) to destination slots.


## -parameters




### -param pSrvName [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The name of the resource for rebinding.


### -param uDstUavSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The first destination slot number for rebinding.


### -param uCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of slots for rebinding. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns:

<ul>
<li><b>S_OK</b> for a valid rebinding</li>
<li><b>S_FALSE</b> for rebinding a nonexistent slot; that is, for which the shader reflection doesn’t have any data</li>
<li><b>E_FAIL</b> for an invalid rebinding, for example, the rebinding is out-of-bounds</li>
<li>Possibly one of the other <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/BBC64078-FCA8-4868-B9CD-3E6F3C86BFC5">ID3D11ModuleInstance</a>
 

 

