---
UID: NF:clfsw32.DumpLogRecords
title: DumpLogRecords function (clfsw32.h)
description: Scans a specified log; filters log records based on record type; and places the records in an output file stream that the caller opens.
helpviewer_keywords: ["ClfsClientRecord","ClfsDataRecord","ClfsNullRecord","ClfsRestartRecord","DumpLogRecords","DumpLogRecords function [Files]","clfsw32/DumpLogRecords","fs.dumplogrecords"]
old-location: fs\dumplogrecords.htm
tech.root: fs
ms.assetid: 221b701b-93d5-4ff3-ae6d-c1b980064629
ms.date: 12/05/2018
ms.keywords: ClfsClientRecord, ClfsDataRecord, ClfsNullRecord, ClfsRestartRecord, DumpLogRecords, DumpLogRecords function [Files], clfsw32/DumpLogRecords, fs.dumplogrecords
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
 - DumpLogRecords
 - clfsw32/DumpLogRecords
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
 - DumpLogRecords
---

# DumpLogRecords function


## -description

Scans a specified log; filters log records based on record type; and places the records in an output file stream that the caller opens.

## -parameters

### -param pwszLogFileName [in]

The name of the log stream. 

This  name is specified when you create the log  by using  <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a>. The following example identifies the format  to use:

<b>log:&lt;</b><i>log name</i><b>&gt;[::&lt;</b><i>log stream name</i><b>&gt;]</b>

&lt;<i>log  name</i>&gt; corresponds to a valid file path in the  file system.

&lt;<i>log stream name</i>&gt; is the unique name of a log stream in the log.

 For more information, see <a href="/previous-versions/windows/desktop/clfs/log-types">Log Types</a>.

### -param fRecordType [in]

The type of records to be read.  

This parameter can be one or more of the following <a href="/previous-versions/windows/desktop/clfs/clfs-record-type-constants">CLFS_RECORD_TYPE Constants</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ClfsNullRecord"></a><a id="clfsnullrecord"></a><a id="CLFSNULLRECORD"></a><dl>
<dt><b>ClfsNullRecord</b></dt>
</dl>
</td>
<td width="60%">
The default record type of <b>ClfsDataRecord</b> is used.

</td>
</tr>
<tr>
<td width="40%"><a id="ClfsDataRecord"></a><a id="clfsdatarecord"></a><a id="CLFSDATARECORD"></a><dl>
<dt><b>ClfsDataRecord</b></dt>
</dl>
</td>
<td width="60%">
User data records are read.

</td>
</tr>
<tr>
<td width="40%"><a id="ClfsRestartRecord"></a><a id="clfsrestartrecord"></a><a id="CLFSRESTARTRECORD"></a><dl>
<dt><b>ClfsRestartRecord</b></dt>
</dl>
</td>
<td width="60%">
Restart records are read.

</td>
</tr>
<tr>
<td width="40%"><a id="ClfsClientRecord"></a><a id="clfsclientrecord"></a><a id="CLFSCLIENTRECORD"></a><dl>
<dt><b>ClfsClientRecord</b></dt>
</dl>
</td>
<td width="60%">
Both restart and data records are read.

</td>
</tr>
<tr>
<td width="40%"><a id="ClfsClientRecord"></a><a id="clfsclientrecord"></a><a id="CLFSCLIENTRECORD"></a><dl>
<dt><b>ClfsClientRecord</b></dt>
</dl>
</td>
<td width="60%">
Specifies a mask for all valid data or restart records.

</td>
</tr>
</table>

### -param plsnStart [in, optional]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a>  that specifies the starting log sequence number (LSN) for the log dump sequence.

If this parameter is specified, the LSN must be the address of a valid log record in the active part of the log; otherwise, the call fails with status <b>ERROR_INVALID_PARAMETER</b>.

If this parameter is not specified, the start of the dump sequence is the beginning of the active log.

### -param plsnEnd [in, optional]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a>  that specifies the LSN  where the dump sequence should end.

If this LSN is past the end of the LSN range, the function returns <b>ERROR_HANDLE_EOF</b>.  

Unlike <i>plsnStart</i>,  this value does not have to be the LSN of a valid record in the active log, but can be any valid LSN.  Only records with an LSN value less than or equal to <i>plsnEnd</i>  are  placed in the output stream.

If this parameter is <b>NULL</b>, the dump function uses the last LSN in the active log (at the head of the log).

### -param pstrmOut [in, optional]

A pointer to an open output  stream   where  the log records are placed.  

If this parameter is not specified, "stdout" is used as the default.

### -param pfnPrintRecord [in, optional]

A user-defined callback routine that formats user-defined buffers and prints them to the output stream <i>pstrmOut</i>.

The <b>DumpLogRecords</b> function natively outputs its internal record headers to <i>pstrmOut</i>, but depends on the user-defined callback to format the user buffers.

If this parameter is <b>NULL</b>,  <b>DumpLogRecords</b>  places user record data in the output stream as hexadecimal digits.

### -param pfnAllocBlock [in, optional]

A callback function that allocates memory for log blocks.  

If this parameter is <b>NULL</b>, Common Log File System (CLFS) provides a default block allocation function.  This parameter cannot be <b>NULL</b> if a block-freeing callback is specified by using the <i>pfnFreeBuffer</i>  parameter.

The following example identifies the  syntax of the block allocation callback function:

<code>typedef PVOID (* CLFS_BLOCK_ALLOCATION) (voidULONG cbBufferSize, PVOID pvUserContext);</code>

### -param pfnFreeBlock [in, optional]

A callback function that   frees log blocks allocated by <i>pfnAllocBuffer</i>.  

If this parameter is <b>NULL</b>, CLFS provides a default block deallocation function.  This parameter cannot be <b>NULL</b> if a block allocation callback is specified by using the <i>pfnAllocBuffer</i> parameter.

The following example identifies the syntax of the  block-freeing callback function:

<code>typedef void (* CLFS_BLOCK_DEALLOCATION) (PVOID pvBuffer, PVOID pvUserContext);</code>

The <i>buffer</i> parameter of "ClfsBlockDeallocProc" must point to a block that is allocated by using the callback pointed to by <i>pfnAllocBuffer</i>.

### -param pvBlockAllocContext [in, optional]

A pointer to a  buffer that is passed as a user context to the block allocation and deallocation routines, if a buffer is specified.  

If <i>pfnAllocBuffer</i> is <b>NULL</b>, this parameter is ignored.

### -param cbBlock [in]

The size of the buffer that your records are marshaled into, in bytes.    

Records cannot be appended or read if they are longer than this value.

### -param cMaxBlocks [in]

The maximum number of blocks that can be allocated at any time for read operations.  

Read contexts use at least one read block.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following list identifies the  possible error codes:

## -see-also

<a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a>



<a href="/previous-versions/windows/desktop/clfs/clfs-record-type-constants">CLFS_RECORD_TYPE</a>



<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>