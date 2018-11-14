---
UID: NF:msports.ComDBClose
title: ComDBClose function
author: windows-sdk-content
description: ComDBClose closes a handle to the COM port database.
old-location: serports\comdbclose.htm
tech.root: serports
ms.assetid: 3ea720ba-6cc9-4862-83d2-4f87e5c13da4
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: ComDBClose, ComDBClose function [Serial Ports], comdb_0274a1cb-0128-48c8-b536-3a10792582f4.xml, msports/ComDBClose, serports.comdbclose
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: msports.h
req.include-header: Msports.h
req.target-type: Desktop
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
req.lib: Msports.lib
req.dll: Msports.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msports.dll
api_name:
 - ComDBClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ComDBClose
: 
---

# ComDBClose function


## -description


<b>ComDBClose</b> closes a handle to the COM port database.


## -parameters




### -param HComDB [in]

Handle to the COM port database that was returned by <a href="https://msdn.microsoft.com/6ae22de0-b71e-441d-af12-8518a3f474e3">ComDBOpen</a>.


## -returns



<b>ComDBClose</b> returns one of the following status values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The COM port database was closed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The specified COM port database handle is not valid.

</td>
</tr>
</table>
 




## -remarks



To open the COM port database, call <b>ComDBOpen</b>.

<b>ComDBOpen</b> is called from user mode.

For more information, see <a href="https://msdn.microsoft.com/c9baf147-6e33-4ed2-b682-c141938eb0da">Opening and Closing the COM Port Database</a>.




## -see-also




<a href="https://msdn.microsoft.com/6ae22de0-b71e-441d-af12-8518a3f474e3">ComDBOpen</a>
 

 

