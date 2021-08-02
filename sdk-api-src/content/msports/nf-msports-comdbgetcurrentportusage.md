---
UID: NF:msports.ComDBGetCurrentPortUsage
title: ComDBGetCurrentPortUsage function (msports.h)
description: ComDBGetCurrentPortUsage returns information about the COM port numbers that are currently logged as &quot;in use&quot; in the COM port database.
helpviewer_keywords: ["ComDBGetCurrentPortUsage","ComDBGetCurrentPortUsage function [Serial Ports]","comdb_b4de1b55-d769-424f-842a-21a8cb28ef1d.xml","msports/ComDBGetCurrentPortUsage","serports.comdbgetcurrentportusage"]
old-location: serports\comdbgetcurrentportusage.htm
tech.root: serports
ms.assetid: f1c5fdc5-b84b-4c7f-832a-44151df39721
ms.date: 12/05/2018
ms.keywords: ComDBGetCurrentPortUsage, ComDBGetCurrentPortUsage function [Serial Ports], comdb_b4de1b55-d769-424f-842a-21a8cb28ef1d.xml, msports/ComDBGetCurrentPortUsage, serports.comdbgetcurrentportusage
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ComDBGetCurrentPortUsage
 - msports/ComDBGetCurrentPortUsage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msports.dll
api_name:
 - ComDBGetCurrentPortUsage
---

# ComDBGetCurrentPortUsage function


## -description

<b>ComDBGetCurrentPortUsage</b> returns information about the COM port numbers that are currently logged as "in use" in the COM port database.

## -parameters

### -param HComDB [in]

Handle to the COM port database that was returned by <a href="/windows/desktop/api/msports/nf-msports-comdbopen">ComDBOpen</a>.

### -param Buffer [out, optional]

Pointer to a caller-allocated buffer in which the routine returns information about COM port number. See the Remarks section for more information.

### -param BufferSize [in]

Specifies the size, in bytes, of a caller-allocated buffer at <i>Buffer</i>.

### -param ReportType [in]

Specifies one of the following flags.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
CDB_REPORT_BITS

</td>
<td>
The routine returns a bit array at <i>Buffer</i> that specifies port number usage.

</td>
</tr>
<tr>
<td>
CDB_REPORT_BYTES

</td>
<td>
The routine returns a byte array at <i>Buffer</i> that specifies port number usage.

</td>
</tr>
</table>

### -param MaxPortsReported [out, optional]

Pointer to the value that the routine uses to return the number of ports for which the routine returns information at <i>Buffer</i>. See the Remarks section for more information.

## -returns

<b>ComDBGetCurrentPortUsage</b> returns one of the following status values.

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
The routine successfully returned port number usage information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the following is true: The specified handle to the COM port database is not valid. Both <i>Buffer</i> and <i>MaxPortsReports</i> are <b>NULL</b>. <i>ReportType</i> is not valid.

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

By setting <i>Buffer</i> to <b>NULL</b> and <i>MaxPortsReported</i> to a valid pointer, a caller can determine the current COM port database size, which is the number of COM port numbers that are currently arbitrated in the database. In this case, the routine sets *<i>MaxPortsReported</i> to the database size. <i>ReportType</i> is not used. 

If <i>Buffer</i> is non-<b>NULL</b> and <i>ReportType</i> is valid, the routine does the following:

<ul>
<li>
If <i>ReportType</i> is CDB_REPORT_BITS, the routine returns a bit array that specifies port number usage. Each bit in the output buffer corresponds to a port number. Using a zero-based index, bit zero of byte zero at <i>Buffer</i> corresponds to COM1, bit 1 corresponds to COM2, and so on. A bit value of 1 indicates that the port number is in use and a value of zero indicates the port number is not in use. The number of port numbers for which the routine returns usage information is the minimum of the current database size and the number of bits in the buffer (<i>BufferSize</i>*8). If <i>MaxPortsReported</i> is non-<b>NULL</b>, the routine also sets *<i>MaxPortsReported</i> to the number of port numbers for which the routine returns usage information. If BufferSize is zero, no port usage information is returned and *<i>MaxPortsReported</i> is set to zero.

</li>
<li>
If <i>ReportType</i> is CDB_REPORT_BYTES, the routine returns a byte array that specifies port number usage. Each byte in the returned information corresponds to a different port number. Using a zero-based index, byte zero at <i>Buffer</i> corresponds to COM1, byte 1 corresponds to COM2, and so on. A byte value of 1 indicates the port number is in use and a value of zero indicates the port number is not in use. The number of port numbers for which the routine returns usage information is the minimum of the current database size and <i>BufferSize</i>. The routine does not set *<i>MaxPortsReported</i>. If <i>BufferSize</i> is zero, no port usage information is returned.

</li>
</ul>
<b>ComDBGetCurrentPortUsage</b> runs in user mode.

## -see-also

<a href="/windows/desktop/api/msports/nf-msports-comdbclaimnextfreeport">ComDBClaimNextFreePort</a>



<a href="/windows/desktop/api/msports/nf-msports-comdbclaimport">ComDBClaimPort</a>



<a href="/windows/desktop/api/msports/nf-msports-comdbresizedatabase">ComDBResizeDatabase</a>