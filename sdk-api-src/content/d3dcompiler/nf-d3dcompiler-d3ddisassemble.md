---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# D3DDisassemble function


## -description


Disassembles compiled HLSL code.


## -parameters




### -param pSrcData [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCVOID</a></b>

A pointer to source data as compiled HLSL code.


### -param SrcDataSize [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">SIZE_T</a></b>

Length of <i>pSrcData</i>.


### -param Flags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Flags affecting the behavior of <b>D3DDisassemble</b>.  <i>Flags</i> can be a combination of zero or more of the following values.
          

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td><b>D3D_DISASM_ENABLE_COLOR_CODE</b></td>
<td>Enable the output of color codes.</td>
</tr>
<tr>
<td><b>D3D_DISASM_ENABLE_DEFAULT_VALUE_PRINTS</b></td>
<td>Enable the output of default values.</td>
</tr>
<tr>
<td><b>D3D_DISASM_ENABLE_INSTRUCTION_NUMBERING</b></td>
<td>Enable instruction numbering.</td>
</tr>
<tr>
<td><b>D3D_DISASM_ENABLE_INSTRUCTION_CYCLE</b></td>
<td>No effect.</td>
</tr>
<tr>
<td><b>D3D_DISASM_DISABLE_DEBUG_INFO</b></td>
<td>Disable debug information.</td>
</tr>
<tr>
<td><b>D3D_DISASM_ENABLE_INSTRUCTION_OFFSET</b></td>
<td>Enable instruction offsets.</td>
</tr>
<tr>
<td><b>D3D_DISASM_INSTRUCTION_ONLY</b></td>
<td>Disassemble instructions only.</td>
</tr>
<tr>
<td><b> D3D_DISASM_PRINT_HEX_LITERALS</b></td>
<td>Use hex symbols in disassemblies.</td>
</tr>
</table>
 


### -param szComments [in, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The comment string at the top of the shader that identifies the shader constants and variables.


### -param ppDisassembly [out]

Type: <b><a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a>**</b>

A pointer to a buffer that receives the <a href="https://msdn.microsoft.com/f6a04778-1ab9-4935-98b8-f814c6b4ebac">ID3DBlob</a> interface that accesses assembly text.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 return codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

