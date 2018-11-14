---
UID: NF:msports.ComDBResizeDatabase
title: ComDBResizeDatabase function
author: windows-sdk-content
description: ComDBResizeDatabase resizes the COM port database.
old-location: serports\comdbresizedatabase.htm
tech.root: serports
ms.assetid: fef761be-57c5-4188-8de9-dbca31d91870
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: ComDBResizeDatabase, ComDBResizeDatabase function [Serial Ports], comdb_b0a32b8b-517e-45af-970a-7f192e5434fb.xml, msports/ComDBResizeDatabase, serports.comdbresizedatabase
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
 - ComDBResizeDatabase
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ComDBResizeDatabase
: 
---

# ComDBResizeDatabase function


## -description


<b>ComDBResizeDatabase</b> resizes the COM port database.


## -parameters




### -param HComDB [in]

Handle to the COM port database that was returned by <a href="https://msdn.microsoft.com/6ae22de0-b71e-441d-af12-8518a3f474e3">ComDBOpen</a>.


### -param NewSize [in]

Specifies a new size for the COM port database, where the database size is the number of port numbers currently arbitrated in the database. This value must be an integer multiple of 1024, must be greater than the current size, and must be less than or equal to COMDB_MAX_PORTS_ARBITRATED.


## -returns



<b>ComDBResizeDatabase</b> returns one of the following status values.

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
The database was successfully resized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_LENGTH</b></dt>
</dl>
</td>
<td width="60%">
<i>NewSize</i> is less than or equal to the current database size, or it is greater than COMDB_MAX_PORTS_ARBITRATED.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANTWRITE</b></dt>
</dl>
</td>
<td width="60%">
The routine could not write to the database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the following is true: The specified handle to the COM port database is not valid. <i>NewSize</i> is not a multiple of 1024.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The routine could not access the database. To get extended error information, call <b>GetLastError</b>.

</td>
</tr>
</table>
 




## -remarks



Use <a href="https://msdn.microsoft.com/f1c5fdc5-b84b-4c7f-832a-44151df39721">ComDBGetCurrentPortUsage</a> to obtain the current database size.

<b>ComDBResizeDatabase</b> runs in user mode.

For more information, see <a href="https://msdn.microsoft.com/c9baf147-6e33-4ed2-b682-c141938eb0da">Resizing the COM Port Database</a>.




## -see-also




<a href="https://msdn.microsoft.com/f1c5fdc5-b84b-4c7f-832a-44151df39721">ComDBGetCurrentPortUsage</a>
 

 

