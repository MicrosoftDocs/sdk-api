---
UID: NF:d3d10.ID3D10Device.IAGetPrimitiveTopology
title: ID3D10Device::IAGetPrimitiveTopology method
author: windows-driver-content
description: Get information about the primitive type, and data order that describes input data for the input assembler stage.
old-location: direct3d10\id3d10device_iagetprimitivetopology.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_iagetprimitivetopology.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: 00286006-d7cd-22c0-fbe8-077a333cce09, IAGetPrimitiveTopology method [Direct3D 10], IAGetPrimitiveTopology method [Direct3D 10], ID3D10Device interface, IAGetPrimitiveTopology,ID3D10Device.IAGetPrimitiveTopology, ID3D10Device, ID3D10Device interface [Direct3D 10], IAGetPrimitiveTopology method, ID3D10Device::IAGetPrimitiveTopology, d3d10/ID3D10Device::IAGetPrimitiveTopology, direct3d10.id3d10device_iagetprimitivetopology
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d10.h
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
req.typenames: D3D10_USAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10.lib
-	D3D10.dll
api_name:
-	ID3D10Device.IAGetPrimitiveTopology
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::IAGetPrimitiveTopology method


## -description


Get information about the <a href="https://msdn.microsoft.com/357ad085-fd91-4420-abc3-1c57e8cbb517">primitive type</a>, and data order that describes input data for the <a href="https://msdn.microsoft.com/71141a5e-2d79-4b02-8370-c0cbc8618908">input assembler</a> stage.


## -parameters




### -param pTopology [out]

Type: <b><a href="https://msdn.microsoft.com/a33b5406-bead-4513-96ef-bb442a18564e">D3D10_PRIMITIVE_TOPOLOGY</a>*</b>

A pointer to the type of primitive, and ordering of the primitive data (see <a href="https://msdn.microsoft.com/a33b5406-bead-4513-96ef-bb442a18564e">D3D10_PRIMITIVE_TOPOLOGY</a>).


## -returns



Returns nothing.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

