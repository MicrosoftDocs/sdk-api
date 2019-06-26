---
UID: NS:d3d12.D3D12_WRITEBUFFERIMMEDIATE_PARAMETER
title: D3D12_WRITEBUFFERIMMEDIATE_PARAMETER (d3d12.h)
author: windows-sdk-content
description: Specifies the immediate value and destination address written using ID3D12CommandList2::WriteBufferImmediate.
old-location: direct3d12\d3d12_writebufferimmediate_parameter.htm
tech.root: direct3d12
ms.assetid: 7CF8A888-BB3A-4557-8DA5-7AFAFC6747CF
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_WRITEBUFFERIMMEDIATE_PARAMETER, D3D12_WRITEBUFFERIMMEDIATE_PARAMETER structure, d3d12/D3D12_WRITEBUFFERIMMEDIATE_PARAMETER, direct3d12.d3d12_writebufferimmediate_parameter
ms.topic: struct
f1_keywords: 
 - "d3d12/D3D12_WRITEBUFFERIMMEDIATE_PARAMETER"
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
 - d3d12.h
api_name:
 - D3D12_WRITEBUFFERIMMEDIATE_PARAMETER
product: Windows
targetos: Windows
req.typenames: D3D12_WRITEBUFFERIMMEDIATE_PARAMETER
req.redist: 
ms.custom: 19H1
---

# D3D12_WRITEBUFFERIMMEDIATE_PARAMETER structure


## -description


Specifies the immediate value and destination address written using <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist2">ID3D12CommandList2::WriteBufferImmediate</a>.


## -struct-fields




### -field Dest

The GPU virtual address at which to write the value. The address must be aligned to a 32-bit (4-byte) boundary.


### -field Value

The 32-bit value to write.


## -remarks








## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
 

 

