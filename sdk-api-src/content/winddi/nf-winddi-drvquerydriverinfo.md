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

# DrvQueryDriverInfo function


## -description


The <b>DrvQueryDriverInfo</b> function returns requested driver-specific information.


## -parameters




### -param dwMode

Caller-supplied constant value, as indicated in the following table.

<table>
<tr>
<th>Value</th>
<th>Definition</th>
</tr>
<tr>
<td>
DRVQUERY_USERMODE

</td>
<td>
The caller is querying whether the driver executes in user mode or in kernel mode.

</td>
</tr>
</table>
 


### -param pBuffer [out]

Caller-supplied pointer to a buffer to receive requested information. The function must supply the following information:

<table>
<tr>
<th><i>dwMode</i> Value</th>
<th><i>pBuffer</i> Size</th>
<th>Value supplied by <b>DrvQueryDriverInfo</b></th>
</tr>
<tr>
<td>
DRVQUERY_USERMODE

</td>
<td>
One DWORD

</td>
<td>
<b>TRUE</b> if driver executes in user mode; <b>FALSE</b> otherwise.

</td>
</tr>
</table>
 


### -param cbBuf

Caller-supplied value representing the size, in bytes, of the buffer pointed to by <i>pBuffer</i>.


### -param pcbNeeded [out]

Caller-supplied pointer to a location to receive the minimum buffer size, in bytes, required to contain the requested information.


## -returns



If the operation succeeds, the function should return <b>TRUE</b>; otherwise it should return <b>FALSE</b>.




## -remarks




<a href="https://msdn.microsoft.com/58e181ff-c792-41a5-967d-a69a8ff5a041">Printer graphics DLLs</a> that execute in user mode must export a <b>DrvQueryDriverInfo</b> function. If the function is not exported, the <a href="https://msdn.microsoft.com/c6f9ba42-5f0f-4919-bfac-e4cd1045de4d">local print provider</a> assumes the graphics DLL executes in kernel mode.



