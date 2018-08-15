---
UID: NF:d3dcompiler.D3DGetTraceInstructionOffsets
title: D3DGetTraceInstructionOffsets function
author: windows-sdk-content
description: Retrieves the byte offsets for instructions within a section of shader code.
old-location: direct3dhlsl\d3dgettraceinstructionoffsets.htm
old-project: direct3dhlsl
ms.assetid: 9E27C70C-C266-48A6-81C7-E9A5E430B48B
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3DGetTraceInstructionOffsets, D3DGetTraceInstructionOffsets function [HLSL], d3dcompiler/D3DGetTraceInstructionOffsets, direct3dhlsl.d3dgettraceinstructionoffsets
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: d3dcompiler.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D_BLOB_PART
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3DCompiler_47.dll
api_name:
 - D3DGetTraceInstructionOffsets
product: Windows
targetos: Windows
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
---

# D3DGetTraceInstructionOffsets function


## -description


Retrieves the byte offsets for instructions within a section of shader code.


## -parameters




### -param pSrcData [in]

A pointer to the compiled shader data.


### -param SrcDataSize [in]

The size, in bytes, of the block of memory that <i>pSrcData</i> points to.


### -param Flags [in]

A combination of the following flags that are combined by using a bitwise <b>OR</b> operation. The resulting value specifies how <b>D3DGetTraceInstructionOffsets</b> retrieves the instruction offsets.

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>D3D_GET_INST_OFFSETS_INCLUDE_NON_EXECUTABLE (0x01)</td>
<td>Include non-executable code in the retrieved information.</td>
</tr>
</table>
 


### -param StartInstIndex [in]

The index of the instruction in the compiled shader data for which <b>D3DGetTraceInstructionOffsets</b> starts to retrieve the byte offsets.


### -param NumInsts [in]

The number of instructions for which <b>D3DGetTraceInstructionOffsets</b> retrieves the byte offsets.


### -param pOffsets [out, optional]

A pointer to a variable that receives the actual number of offsets.


### -param pTotalInsts [out, optional]

A pointer to a variable that receives the total number of instructions in the section of shader code.


## -returns



Returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 return codes</a>.




## -remarks



A new kind of Microsoft High Level Shader Language (HLSL) debugging information from a program database (PDB) file uses instruction-byte offsets within a shader blob (arbitrary-length data buffer). You use <b>D3DGetTraceInstructionOffsets</b> to translate to and from instruction indexes.

<div class="alert"><b>Note</b>  The D3dcompiler_44.dll or later version of the file contains the <b>D3DGetTraceInstructionOffsets</b> compiler function.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/aacc5207-3ec8-4031-b5c9-f7c0fb7b7095">Functions</a>
 

 

