---
UID: NS:d3d12.D3D12_DXIL_LIBRARY_DESC
title: D3D12_DXIL_LIBRARY_DESC
author: windows-sdk-content
description: Describes a DXIL library state subobject that can be included in a state object.
old-location: direct3d12\d3d12_dxil_library_desc.htm
tech.root: direct3d12
ms.assetid: C21E91D4-C307-40D8-A82E-DDB542C1D346
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: D3D12_DXIL_LIBRARY_DESC, D3D12_DXIL_LIBRARY_DESC structure, PD3D12_DXIL_LIBRARY_DESC, PD3D12_DXIL_LIBRARY_DESC structure pointer, d3d12/D3D12_DXIL_LIBRARY_DESC, d3d12/PD3D12_DXIL_LIBRARY_DESC, direct3d12.d3d12_dxil_library_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_DXIL_LIBRARY_DESC
product: Windows
targetos: Windows
req.typenames: D3D12_DXIL_LIBRARY_DESC
req.redist: 
---

# D3D12_DXIL_LIBRARY_DESC structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Describes a DXIL library state subobject that can be included in a state object.


## -struct-fields




### -field DXILLibrary

The library to include in the state object.  Must have been compiled with library target 6.3 or higher.  It is fine to specify the same library multiple times either in the same state object / collection or across multiple, as long as the names exported each time don’t conflict in a given state object.


### -field NumExports

The size of <i>pExports</i> array.  If 0, everything gets exported from the library.



#### pExports

Optional exports array.  For more information, see <a href="http://docs.microsoft.com/windows/desktop/d3d12/ns-d3d12-d3d12_export_desc">D3D12_EXPORT_DESC</a>.


### -field pExports

 



