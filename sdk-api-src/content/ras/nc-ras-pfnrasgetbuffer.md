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

# PFNRASGETBUFFER callback function


## -description


The custom-scripting DLL calls 
<i>RasGetBuffer</i> to allocate memory for sending or receiving data over the port connected to the server. 
		


## -parameters




### -param *ppBuffer

Pointer to a pointer that receives the address of the returned buffer.


### -param pdwSize

Pointer to a <b>DWORD</b> variable that, on input, contains the requested size of the buffer. On output, this variable contains the actual size of the buffer allocated.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is the following error code.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OUT_OF_BUFFERS</b></dt>
</dl>
</td>
<td width="60%">
RAS cannot allocate anymore buffer space.

</td>
</tr>
</table>
 




## -remarks



The maximum buffer size that can be obtained is 1500 bytes.

The custom-scripting DLL calls 
<i>RasGetBuffer</i> through a function pointer. The function pointer is passed to the custom-scripting DLL as a parameter when RAS calls the DLL's implementation of 
<a href="https://msdn.microsoft.com/e31ab530-cb60-4bb0-be44-3ba90fdf71f1">RasCustomScriptExecute</a>.




## -see-also




<a href="https://msdn.microsoft.com/c27b8b02-6018-4441-a355-1fb890b9001c">RAS Custom-Scripting</a>



<a href="https://msdn.microsoft.com/e31ab530-cb60-4bb0-be44-3ba90fdf71f1">RasCustomScriptExecute</a>



<a href="https://msdn.microsoft.com/aba43ef9-7f62-48ab-a790-c8592a57f2c2">RasFreeBuffer</a>
 

 

