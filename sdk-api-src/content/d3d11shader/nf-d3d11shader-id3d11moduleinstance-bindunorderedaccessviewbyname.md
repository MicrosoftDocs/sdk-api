---
UID: NF:d3d11shader.ID3D11ModuleInstance.BindUnorderedAccessViewByName
title: ID3D11ModuleInstance::BindUnorderedAccessViewByName
author: windows-sdk-content
description: Rebinds an unordered access view (UAV) by name to destination slots.
old-location: direct3d11\id3d11moduleinstance_bindunorderedaccessviewbyname.htm
old-project: direct3d11
ms.assetid: 439C12FD-4BAE-4609-88D3-D7B006816716
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: BindUnorderedAccessViewByName, BindUnorderedAccessViewByName method [Direct3D 11], BindUnorderedAccessViewByName method [Direct3D 11],ID3D11ModuleInstance interface, ID3D11ModuleInstance interface [Direct3D 11],BindUnorderedAccessViewByName method, ID3D11ModuleInstance.BindUnorderedAccessViewByName, ID3D11ModuleInstance::BindUnorderedAccessViewByName, d3d11shader/ID3D11ModuleInstance::BindUnorderedAccessViewByName, direct3d11.id3d11moduleinstance_bindunorderedaccessviewbyname
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: D3D11_SHADER_VERSION_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3DCompiler_47.dll
api_name:
-	ID3D11ModuleInstance.BindUnorderedAccessViewByName
product: Windows
targetos: Windows
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# ID3D11ModuleInstance::BindUnorderedAccessViewByName


## -description


Rebinds an unordered access view (UAV) by name to destination slots.


## -parameters




### -param pName [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The name of the UAV for rebinding.


### -param uDstSlot [in]

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
 

 

