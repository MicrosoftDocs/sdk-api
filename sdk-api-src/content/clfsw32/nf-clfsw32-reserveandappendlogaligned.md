---
UID: NF:clfsw32.ReserveAndAppendLogAligned
title: ReserveAndAppendLogAligned function
author: windows-sdk-content
description: Reserves space for log buffers, or appends a log record to the log, or both.
old-location: fs\reserveandappendlogaligned.htm
tech.root: Clfs
ms.assetid: fce678e3-3b30-4bb9-ab61-d7c8b24fd1d7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CLFS_FLAG_FORCE_APPEND, CLFS_FLAG_FORCE_FLUSH, CLFS_FLAG_NO_FLAGS, CLFS_FLAG_USE_RESERVATION, ReserveAndAppendLogAligned, ReserveAndAppendLogAligned function [Files], clfsw32/ReserveAndAppendLogAligned, fs.reserveandappendlogaligned
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clfsw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - ReserveAndAppendLogAligned
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ReserveAndAppendLogAligned
: 
---

# ReserveAndAppendLogAligned function


## -description


Reserves space for log buffers, or appends a log record  to the log, or both.  This function is like the <a href="https://msdn.microsoft.com/2036fc26-d040-4738-b66e-d5d3d0dbe385">ReserveAndAppendLog</a> function, but <b>ReserveAndAppendLogAligned</b> aligns the  write entries of the record to the specified byte alignment.


## -parameters




### -param pvMarshal [in]

A pointer to a   marshaling context that  is allocated by using the <a href="https://msdn.microsoft.com/750c0615-bfac-402b-a590-6c9d800cf2d8">CreateLogMarshallingArea</a> function.


### -param rgWriteEntries [in, optional]

A pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/Bb540357(v=VS.85).aspx">CLFS_WRITE_ENTRY</a> buffers to be marshaled into  one  record.  

This parameter is ignored if the <i>cWriteEntries</i> parameter is zero.


### -param cWriteEntries [in]

The number of write entries  in the <i>rgWriteEntries</i>  array. 

If this value is nonzero, you must specify a buffer in the <i>rgWriteEntries</i> parameter.


### -param cbEntryAlignment [in]

The byte alignment for each write entry in the <i>rgWriteEntries</i> parameter.

Specify 1 (one) for a simple concatenation. The <i>cbWriteEntryAlignment</i> parameter must be nonzero.


### -param plsnUndoNext [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb540343(v=VS.85).aspx">CLFS_LSN</a> structure that specifies the log sequence number (LSN) of the next record in the undo-chain.


### -param plsnPrevious [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb540343(v=VS.85).aspx">CLFS_LSN</a> structure that specifies the LSN of the previous record in the previous-chain.


### -param cReserveRecords [in]

The number of record sizes in the <i>rgcbReservation</i> array.


### -param rgcbReservation [in, out, optional]

A pointer to an array of reservation sizes for each record  that  the <i>cReserveRecords</i> parameter specifies.  

 This parameter is ignored if the <i>cReserveRecords</i> parameter is zero.    If a reservation size is negative, a reservation of that size is released.

The actual space that is reserved for each record, including required overhead, is returned in the individual array elements on successful completion. These values can  be passed to the <a href="https://msdn.microsoft.com/a5e71e4c-5871-4bea-a4a5-a56c7e70276b">FreeReservedLog</a>  function to adjust space that is reserved in the marshaling area.


### -param fFlags [in]

The flags that specify the behavior of this function.  

One or more of the following values can be combined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CLFS_FLAG_FORCE_APPEND"></a><a id="clfs_flag_force_append"></a><dl>
<dt><b>CLFS_FLAG_FORCE_APPEND</b></dt>
</dl>
</td>
<td width="60%">
Assigns a physical location for all appended records in the log that are not previously assigned a physical location.  

All these records are made available for reading from other marshaling contexts.

</td>
</tr>
<tr>
<td width="40%"><a id="CLFS_FLAG_FORCE_FLUSH"></a><a id="clfs_flag_force_flush"></a><dl>
<dt><b>CLFS_FLAG_FORCE_FLUSH</b></dt>
</dl>
</td>
<td width="60%">
Assigns a physical location for all appended records in the log that are not previously assigned a physical location.  

All these records are made available for reading from other marshaling contexts. Then, the records are flushed to disk.

</td>
</tr>
<tr>
<td width="40%"><a id="CLFS_FLAG_NO_FLAGS"></a><a id="clfs_flag_no_flags"></a><dl>
<dt><b>CLFS_FLAG_NO_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
Assigns no flags.

</td>
</tr>
<tr>
<td width="40%"><a id="CLFS_FLAG_USE_RESERVATION"></a><a id="clfs_flag_use_reservation"></a><dl>
<dt><b>CLFS_FLAG_USE_RESERVATION</b></dt>
</dl>
</td>
<td width="60%">
  Appends the current record by using the space  that is reserved in the  marshaling area.

</td>
</tr>
</table>
 


### -param plsn [out, optional]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb540343(v=VS.85).aspx">CLFS_LSN</a> structure that receives the LSN  of the appended record.


### -param pOverlapped

TBD




#### - overlapped [in, out, optional]

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms684342(v=VS.85).aspx">OVERLAPPED</a> structure. 

This parameter can be <b>NULL</b> if asynchronous operation is not used.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. The following list identifies the possible error codes:




## -remarks



The LSN that is returned by the <b>ReserveAndAppendLogAligned</b> function is not necessarily the next LSN that is used.  The LSN that is returned is an estimate of the next LSN, and it varies based on which flags are specified by the <i>fFlags</i> parameter.  The LSN that is returned can be used when moving the base tail.  This LSN is invalidated by the next call to this function.

If the <b>ReserveAndAppendLogAligned</b> function returns <b>ERROR_LOG_FILE_FULL</b>, there is no more space in the log. This can be resolved in one of the following ways:<ul>
<li>Free any unneeded reservations.</li>
<li>Advance the base LSN or the log archive tail, or both, to recycle containers.</li>
<li>Add containers to the log.</li>
</ul>The <a href="https://msdn.microsoft.com/e410afd4-360d-4d3c-a41d-02eb7edda489">CLFS Management API</a> also provides a way to handle scenarios involving  full logs.

If the <b>ReserveAndAppendLogAligned</b>  function is called with a valid <i>overlapped</i> structure and the log handle is created with the overlapped option, then if a call to this function fails with an error code of <b>ERROR_IO_PENDING</b>, a pointer to a valid read context  is  placed in the variable that is pointed to by the <i>ppvReadContext</i> parameter.

To complete the log-record copy, the client should first synchronize its execution with deferred completion of the overlapped I/O operation by using  the <a href="https://msdn.microsoft.com/en-us/library/ms683209(v=VS.85).aspx">GetOverlappedResult</a> function or one of the synchronization <a href="https://msdn.microsoft.com/en-us/library/ms687069(v=VS.85).aspx">Wait Functions</a>. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms686358(v=VS.85).aspx">Synchronization and Overlapped Input and Output</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb540343(v=VS.85).aspx">CLFS_LSN</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb540357(v=VS.85).aspx">CLFS_WRITE_ENTRY</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb540361(v=VS.85).aspx">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms684342(v=VS.85).aspx">OVERLAPPED</a>
 

 

