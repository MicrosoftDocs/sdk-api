---
UID: NF:d3d11.ID3D11DeviceContext.IAGetPrimitiveTopology
title: ID3D11DeviceContext::IAGetPrimitiveTopology
author: windows-sdk-content
description: Get information about the primitive type, and data order that describes input data for the input assembler stage.
old-location: direct3d11\id3d11devicecontext_iagetprimitivetopology.htm
tech.root: direct3d11
ms.assetid: 99f82993-72c2-47b5-a2fe-16bb1e7bd2e3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 83077387-5c62-f840-c94a-b5edcab58593, IAGetPrimitiveTopology, IAGetPrimitiveTopology method [Direct3D 11], IAGetPrimitiveTopology method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],IAGetPrimitiveTopology method, ID3D11DeviceContext.IAGetPrimitiveTopology, ID3D11DeviceContext::IAGetPrimitiveTopology, d3d11/ID3D11DeviceContext::IAGetPrimitiveTopology, direct3d11.id3d11devicecontext_iagetprimitivetopology
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.IAGetPrimitiveTopology
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11.h
: 
- ID3D11DeviceContext.IAGetPrimitiveTopology
: 
---

# ID3D11DeviceContext::IAGetPrimitiveTopology


## -description


Get information about the primitive type, and data order that describes input data for the input assembler stage.


## -parameters




### -param pTopology [out]

Type: <b><a href="https://msdn.microsoft.com/ca0547b2-d0f8-4edc-a62c-3c903e1b33ea">D3D11_PRIMITIVE_TOPOLOGY</a>*</b>

A pointer to the type of primitive, and ordering of the primitive data (see <a href="https://msdn.microsoft.com/ca0547b2-d0f8-4edc-a62c-3c903e1b33ea">D3D11_PRIMITIVE_TOPOLOGY</a>).


## -returns



Returns nothing.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

