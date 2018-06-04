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

# D3D11_TRACE_VALUE structure


## -description


Describes a trace value.


## -struct-fields




### -field Bits


              An array of bits that make up the trace value. The [0] element is X.
            

<div class="alert"><b>Note</b>  
              This member can hold <b>float</b>, <b>UINT</b>, or <b>INT</b> data.
              The elements are specified as <b>UINT</b> rather than using a union to minimize the risk of x86 SNaN-&gt;QNaN quashing during float assignment.
              If the bits are displayed, they can be interpreted as <b>float</b> at the last moment.
            </div>
<div> </div>

### -field ValidMask


            A combination of the following component values that are combined by using a bitwise <b>OR</b> operation.
            The resulting value specifies the component trace mask.
            

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>D3D11_TRACE_COMPONENT_X (0x1)</td>
<td>The x component of the trace mask.</td>
</tr>
<tr>
<td>D3D11_TRACE_COMPONENT_Y (0x2)</td>
<td>The y component of the trace mask.</td>
</tr>
<tr>
<td>D3D11_TRACE_COMPONENT_Z (0x4)</td>
<td>The depth z component of the trace mask.</td>
</tr>
<tr>
<td>D3D11_TRACE_COMPONENT_W (0x8)</td>
<td>The depth w component of the trace mask.</td>
</tr>
</table>
 

Ignore unmasked values, particularly if deltas are accumulated.
          


## -remarks




        This API requires the Windows Software Development Kit (SDK) for Windows 8.
      




## -see-also




<a href="https://msdn.microsoft.com/3b8ece5c-5065-4711-b12c-06cf7ea0e1ba">Shader Structures</a>
 

 

