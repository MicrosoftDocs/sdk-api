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

# FDICreate function


## -description


The <b>FDICreate</b> function creates an FDI context.


## -parameters




### -param pfnalloc [in]

Pointer to an application-defined callback function to allocate memory. The function should be declared using the <a href="https://msdn.microsoft.com/3104267d-3efd-40da-a8b6-af2acf379ff8">FNALLOC</a> macro.


### -param pfnfree [in]

Pointer to an application-defined callback function to free previously allocated memory. The function should be declared using the <a href="https://msdn.microsoft.com/646a0cb4-1f3a-42a1-a508-12d80bdb4a01">FNFREE</a> macro.


### -param pfnopen [in]

Pointer to an application-defined callback function to open a file. The function should be declared using the <a href="https://msdn.microsoft.com/45bd2d23-1f6d-42a6-8afb-86227da6118f">FNOPEN</a> macro.


### -param pfnread [in]

Pointer to an application-defined callback function to read data from a file. The function should be declared using the <a href="https://msdn.microsoft.com/0a8c6c9f-051c-43a0-b43b-1fd8b4fef10c">FNREAD</a> macro.


### -param pfnwrite [in]

Pointer to an application-defined callback function to write data to a file. The function should be declared using the <a href="https://msdn.microsoft.com/e15d4293-2955-48cd-b8c9-77669a1e6436">FNWRITE</a> macro.


### -param pfnclose [in]

Pointer to an application-defined callback function to close a file. The function should be declared using the <a href="https://msdn.microsoft.com/89db9c2a-42ab-410d-a427-60d282385c2b">FNCLOSE</a> macro.


### -param pfnseek [in]

Pointer to an application-defined callback function to move a file pointer to the specified location. The function should be declared using the <a href="https://msdn.microsoft.com/e49b5086-6b89-40ce-b6fa-905d21593dec">FNSEEK</a> macro.


### -param cpuType [in]

In the 16-bit version of FDI, specifies the CPU type and can be any of the following values.

<div class="alert"><b>Note</b>  Expressing the <b>cpuUNKNOWN</b> value is recommended.</div>
<div> </div>
<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="cpuUNKNOWN"></a><a id="cpuunknown"></a><a id="CPUUNKNOWN"></a><dl>
<dt><b>cpuUNKNOWN</b></dt>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
FDI should determine the CPU type.

</td>
</tr>
<tr>
<td width="40%"><a id="cpu80286"></a><a id="CPU80286"></a><dl>
<dt><b>cpu80286</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Only 80286 instructions can be used.

</td>
</tr>
<tr>
<td width="40%"><a id="cpu80386"></a><a id="CPU80386"></a><dl>
<dt><b>cpu80386</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
80386 instructions can be used.

</td>
</tr>
</table>
 


### -param perf [in, out]

Pointer to an <a href="https://msdn.microsoft.com/ddbccad9-a68c-4be7-90dc-e3dd25f5cf3b">ERF</a> structure that receives the error information.


## -returns



If the function succeeds, it returns a non-<b>NULL</b> HFDI context pointer; otherwise, it returns <b>NULL</b>.

Extended error information is provided in the <a href="https://msdn.microsoft.com/ddbccad9-a68c-4be7-90dc-e3dd25f5cf3b">ERF</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/fe3b8045-a476-4a21-b732-0d4799798faf">FDIDestroy</a>
 

 

