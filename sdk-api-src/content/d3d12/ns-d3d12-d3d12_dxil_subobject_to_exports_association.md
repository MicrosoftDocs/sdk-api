---
UID: NS:d3d12.D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION
title: D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION
author: windows-sdk-content
description: This subobject is unsupported in the current release.
old-location: direct3d12\d3d12_dxil_subobject_to_exports_association.htm
tech.root: direct3d12
ms.assetid: 82990FE6-43A8-4597-BAC5-E995B1FA67EB
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION, D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION structure, PD3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION, PD3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION structure pointer, d3d12/D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION, d3d12/PD3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION, direct3d12.d3d12_dxil_subobject_to_exports_association
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
 - D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION
product: Windows
targetos: Windows
req.typenames: D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION
req.redist: 
---

# D3D12_DXIL_SUBOBJECT_TO_EXPORTS_ASSOCIATION structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

This subobject is unsupported in the current release.


## -struct-fields




### -field SubobjectToAssociate

 


### -field NumExports

Size of the <i>pExports</i> array.  If 0, this is being explicitly defined as a default association.  Another way to define a default association is to omit this subobject association for that subobject completely.



#### pExports

The array of exports with which the subobject is associated.


### -field pExports

 




#### - pDXILSubobjectName

Name of the subobject defined in a DXIL library to define an association to.

