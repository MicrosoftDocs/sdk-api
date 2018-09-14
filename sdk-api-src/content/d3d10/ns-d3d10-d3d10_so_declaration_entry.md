---
UID: NS:d3d10.D3D10_SO_DECLARATION_ENTRY
title: D3D10_SO_DECLARATION_ENTRY
author: windows-sdk-content
description: Description of a vertex element in a vertex buffer in an output slot.
old-location: direct3d10\d3d10_so_declaration_entry.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_so_declaration_entry.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: 367a5fa7-5907-24fc-2124-92ee48f50140, D3D10_SO_DECLARATION_ENTRY, D3D10_SO_DECLARATION_ENTRY structure [Direct3D 10], d3d10/D3D10_SO_DECLARATION_ENTRY, direct3d10.d3d10_so_declaration_entry
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_SO_DECLARATION_ENTRY
product: Windows
targetos: Windows
req.typenames: D3D10_SO_DECLARATION_ENTRY
req.redist: 
---

# D3D10_SO_DECLARATION_ENTRY structure


## -description


Description of a vertex element in a vertex buffer in an output slot.


## -struct-fields




### -field SemanticName

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

Type of output element.  Possible values: "POSITION", "NORMAL", or "TEXCOORD0".


### -field SemanticIndex

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Output element's zero-based index. Should be used if, for example, you have more than one texture coordinate stored in each vertex.


### -field StartComponent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

Which component of the entry to begin writing out to. Valid values are 0 ~ 3. For example, if you only wish to output to the y and z components of a position, then StartComponent should be 1 and ComponentCount should be 2.


### -field ComponentCount

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

The number of components of the entry to write out to. Valid values are 1 ~ 4. For example, if you only wish to output to the y and z components of a position, then StartComponent should be 1 and ComponentCount should be 2.


### -field OutputSlot

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BYTE</a></b>

The output slot that contains the vertex buffer that contains this output entry.


## -see-also




<a href="https://msdn.microsoft.com/84769515-3f3b-4464-9620-7b806bf905b3">Core Structures</a>
 

 

