---
UID: NF:clfsw32.WriteLogRestartArea
title: WriteLogRestartArea function (clfsw32.h)
description: Appends a new client restart area to a log, and optionally advances the base log sequence number (LSN) of the log.
helpviewer_keywords: ["CLFS_FLAG_NO_FLAGS","CLFS_FLAG_USE_RESERVATION","WriteLogRestartArea","WriteLogRestartArea function [Files]","clfsw32/WriteLogRestartArea","fs.writelogrestartarea"]
old-location: fs\writelogrestartarea.htm
tech.root: fs
ms.assetid: deb5fd90-e987-4e5b-9740-6ecef8705557
ms.date: 12/05/2018
ms.keywords: CLFS_FLAG_NO_FLAGS, CLFS_FLAG_USE_RESERVATION, WriteLogRestartArea, WriteLogRestartArea function [Files], clfsw32/WriteLogRestartArea, fs.writelogrestartarea
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WriteLogRestartArea
 - clfsw32/WriteLogRestartArea
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - WriteLogRestartArea
---

# WriteLogRestartArea function


## -description

Appends a new client restart area to a log, and optionally advances the base log sequence number (LSN) of the log.

After it is successfully written to a disk, the last LSN of the log is changed to the LSN of the appended restart record.   Typically, <b>WriteLogRestartArea</b> is  used by applications that regularly save a known good state, and the restart area contains the LSNs for existing log record chains.

## -parameters

### -param pvMarshal [in, out]

A pointer to the   marshaling context that is allocated by using the <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogmarshallingarea">CreateLogMarshallingArea</a> function.

### -param pvRestartBuffer [in]

A pointer to a  buffer that contains restart data.

### -param cbRestartBuffer [in]

The size of <i>pvRestartBuffer</i>, in bytes.

### -param plsnBase [in, optional]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure that specifies the new base LSN of the log after successfully writing the restart area.  

This value cannot be outside the range of the active log. It must be at least the value of the current base LSN, and not greater than the LSN that was returned in the <i>lastLSN</i> parameter from the latest call to <a href="/windows/desktop/api/clfsw32/nf-clfsw32-reserveandappendlog">ReserveAndAppendLog</a>.  If you omit this optional parameter, the base LSN  does not change.

### -param fFlags [in]

The flags that specify the behavior of this function.  

One or more of the following values can be combined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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

### -param pcbWritten [out, optional]

A pointer to a variable that receives the number of bytes that are  written when an operation completes.

### -param plsnNext [out, optional]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure that specifies the LSN of the restart area that is written.

### -param pOverlapped [in, out, optional]

A pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. 

This parameter can be <b>NULL</b> if an asynchronous operation is not used.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following  list identifies the possible error codes:

## -remarks

The <b>WriteLogRestartArea</b> causes both a flush of all current buffered log records and a flush of the log metadata.

If a client calls <b>WriteLogRestartArea</b> on  a  log  that is created to support asynchronous operations (for example, if the <i>fFlagsAndAttributes</i> parameter of <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a>  is set to <b>FILE_FLAG_OVERLAPPED</b> when the log is created), the client must supply a pointer to a valid <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure in the <i>pOverlapped</i> parameter of <b>WriteLogRestartArea</b>.

Then, if  <b>WriteLogRestartArea</b>   fails with an error of <b>ERROR_IO_PENDING</b>, a pointer to a valid read context is placed in the variable that is pointed to by the <i>ppvReadContext</i> parameter. 

To complete the call, the client should synchronize its execution with deferred completion of the overlapped I/O operation by using <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> or one of the synchronization <a href="/windows/desktop/Sync/wait-functions">Wait Functions</a>. For more information, see <a href="/windows/desktop/Sync/synchronization-and-overlapped-input-and-output">Synchronization and Overlapped Input and Output</a>.

## -see-also

<a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a>



<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>