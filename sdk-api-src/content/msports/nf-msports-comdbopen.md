---
UID: NF:msports.ComDBOpen
title: ComDBOpen function
author: windows-driver-content
description: ComDBOpen returns a handle to the COM port database.
old-location: serports\comdbopen.htm
old-project: serports
ms.assetid: 6ae22de0-b71e-441d-af12-8518a3f474e3
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: ComDBOpen, ComDBOpen function [Serial Ports], comdb_ab14e7a4-69f0-42fc-82b5-df6f5863779a.xml, msports/ComDBOpen, serports.comdbopen
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
req.typenames: MSPEVENTITEM, *PMSPEVENTITEM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msports.dll
api_name:
-	ComDBOpen
product: Windows
targetos: Windows
req.lib: Msports.lib
req.dll: Msports.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ComDBOpen function


## -description


<b>ComDBOpen</b> returns a handle to the COM port database.


## -parameters




### -param PHComDB [out]

Pointer, if the routine succeeds, to a handle to the COM port database. Otherwise, the routine sets <i>*PHComDB</i> to <b>HCOMDB_INVALID_HANDLE_VALUE</b>. <i>PHComDB</i> must be non-NULL.


## -returns



<b>ComDBOpen</b> returns one of the following status values.

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
The COM port database was successfully opened.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The routine could not open the database. To get extended error information, call <b>GetLastError</b>.

</td>
</tr>
</table>
 




## -remarks



To close the COM port database, call <a href="https://msdn.microsoft.com/library/windows/hardware/ff546473">ComDBClose</a> and supply the handle that was returned by <b>ComDBOpen</b>.

<b>ComDBOpen</b> is called from user mode.

For more information, see <a href="https://msdn.microsoft.com/c9baf147-6e33-4ed2-b682-c141938eb0da">Opening and Closing the COM Port Database</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546473">ComDBClose</a>
 

 

