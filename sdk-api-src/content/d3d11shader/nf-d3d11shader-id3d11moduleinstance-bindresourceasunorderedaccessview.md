---
UID: NF:d3d11shader.ID3D11ModuleInstance.BindResourceAsUnorderedAccessView
title: ID3D11ModuleInstance::BindResourceAsUnorderedAccessView
author: windows-sdk-content
description: Rebinds a resource as an unordered access view (UAV) from source slot to destination slot.
old-location: direct3d11\id3d11moduleinstance_bindresourceasunorderedaccessview.htm
tech.root: direct3d11
ms.assetid: A9E61E17-F1FE-4BF1-8A4A-F73B23FEDD08
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BindResourceAsUnorderedAccessView, BindResourceAsUnorderedAccessView method [Direct3D 11], BindResourceAsUnorderedAccessView method [Direct3D 11],ID3D11ModuleInstance interface, ID3D11ModuleInstance interface [Direct3D 11],BindResourceAsUnorderedAccessView method, ID3D11ModuleInstance.BindResourceAsUnorderedAccessView, ID3D11ModuleInstance::BindResourceAsUnorderedAccessView, d3d11shader/ID3D11ModuleInstance::BindResourceAsUnorderedAccessView, direct3d11.id3d11moduleinstance_bindresourceasunorderedaccessview
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
 - ID3D11ModuleInstance.BindResourceAsUnorderedAccessView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11ModuleInstance::BindResourceAsUnorderedAccessView


## -description


Rebinds a resource as an unordered access view (UAV) from source slot to destination slot.


## -parameters




### -param uSrcSrvSlot [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The first source slot number for rebinding.


### -param uDstUavSlot [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The first destination slot number for rebinding.


### -param uCount [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The number of slots for rebinding. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns:

<ul>
<li><b>S_OK</b> for a valid rebinding</li>
<li><b>S_FALSE</b> for rebinding a nonexistent slot; that is, for which the shader reflection doesn’t have any data</li>
<li><b>E_FAIL</b> for an invalid rebinding, for example, the rebinding is out-of-bounds</li>
<li>Possibly one of the other <a href="https://msdn.microsoft.com/en-us/library/Ff476174(v=VS.85).aspx">Direct3D 11 Return Codes</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn280564(v=VS.85).aspx">ID3D11ModuleInstance</a>
 

 

