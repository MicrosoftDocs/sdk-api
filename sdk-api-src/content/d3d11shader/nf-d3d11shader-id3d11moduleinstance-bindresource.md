---
UID: NF:d3d11shader.ID3D11ModuleInstance.BindResource
title: ID3D11ModuleInstance::BindResource (d3d11shader.h)
author: windows-sdk-content
description: Rebinds a texture or buffer from source slot to destination slot.
old-location: direct3d11\id3d11moduleinstance_bindresource.htm
tech.root: direct3d11
ms.assetid: 7EBF623B-1C04-43C5-A262-62EA125D6631
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BindResource, BindResource method [Direct3D 11], BindResource method [Direct3D 11],ID3D11ModuleInstance interface, ID3D11ModuleInstance interface [Direct3D 11],BindResource method, ID3D11ModuleInstance.BindResource, ID3D11ModuleInstance::BindResource, d3d11shader/ID3D11ModuleInstance::BindResource, direct3d11.id3d11moduleinstance_bindresource
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
 - ID3D11ModuleInstance.BindResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11ModuleInstance::BindResource


## -description


Rebinds a texture or buffer from source slot to destination slot.


## -parameters




### -param uSrcSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The first source slot number for rebinding.


### -param uDstSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The first destination slot number for rebinding.


### -param uCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of slots for rebinding. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

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
 

 

