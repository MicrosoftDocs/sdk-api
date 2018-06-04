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

# D3D11_TRACE_REGISTER structure


## -description


Describes a trace register.


## -struct-fields




### -field RegType


            A <a href="https://msdn.microsoft.com/94B0BA0B-94DB-4449-8E3B-EEB1F6B85FB5">D3D11_TRACE_REGISTER_TYPE</a>-typed value that identifies the type of register that the shader-trace object uses.
          


### -field Index1D

An index for one-dimensional arrays. This index is used by the following register types: 

<ul>
<li>vertex shader or pixel shader input: v[Index1D]</li>
<li>temp: r[Index1D]</li>
<li>output: o[Index1D]</li>
<li>immediate constant buffer: icb[Index1D]</li>
<li>sampler s[Index1D]</li>
<li>resource r[Index1D]</li>
<li>input patch constant register: vpc[Index1D] </li>
<li>unordered access view: u[Index1D]</li>
<li>thread group shared memory: g[Index1D]</li>
</ul>

### -field Index2D

An array of indexes for two-dimensional arrays. These indexes are used by the following register types:

<ul>
<li>GS input: v[Index2D[0]][Index2D[1]]</li>
<li>indexable temp: x[Index2D[0]][Index2D[1]]</li>
<li>constant buffer: cb#[#]</li>
<li>input control point register: vcp[Index2D[0]][Index2D[1]]</li>
<li>output control point register: vocp[Index2D[0]][Index2D[1]]</li>
</ul>

### -field OperandIndex

The index of the operand, which starts from 0.


### -field Flags


            A combination of the following flags that are combined by using a bitwise <b>OR</b> operation. The resulting value specifies more about the trace register.

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>D3D11_TRACE_REGISTER_FLAGS_RELATIVE_INDEXING (0x1)</td>
<td>Access to the register is part of the relative indexing of a register.</td>
</tr>
</table>
 


## -remarks



The following register types do not require an index:

<ul>
<li>input PrimitiveID</li>
<li>output oDepth</li>
<li>immediate32</li>
<li>NULL register</li>
<li>output control point ID (this is actually an input; it defines the output that the thread controls)</li>
<li>input fork instance ID</li>
<li>input join instance ID</li>
<li>input domain point register</li>
<li>cycle counter</li>
</ul>
<div class="alert"><b>Note</b>  
        This API requires the Windows Software Development Kit (SDK) for Windows 8.
      </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/3b8ece5c-5065-4711-b12c-06cf7ea0e1ba">Shader Structures</a>
 

 

