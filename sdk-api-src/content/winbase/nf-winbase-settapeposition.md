---
UID: NF:winbase.SetTapePosition
title: SetTapePosition function (winbase.h)
description: Sets the tape position on the specified device.
helpviewer_keywords: ["SetTapePosition","SetTapePosition function [Backup]","TAPE_ABSOLUTE_BLOCK","TAPE_LOGICAL_BLOCK","TAPE_REWIND","TAPE_SPACE_END_OF_DATA","TAPE_SPACE_FILEMARKS","TAPE_SPACE_RELATIVE_BLOCKS","TAPE_SPACE_SEQUENTIAL_FMKS","TAPE_SPACE_SEQUENTIAL_SMKS","TAPE_SPACE_SETMARKS","_win32_settapeposition","backup.settapeposition","base.settapeposition","winbase/SetTapePosition"]
old-location: backup\settapeposition.htm
tech.root: Backup
ms.assetid: e1962aa5-c187-4fef-886c-36a8b096829f
ms.date: 12/05/2018
ms.keywords: SetTapePosition, SetTapePosition function [Backup], TAPE_ABSOLUTE_BLOCK, TAPE_LOGICAL_BLOCK, TAPE_REWIND, TAPE_SPACE_END_OF_DATA, TAPE_SPACE_FILEMARKS, TAPE_SPACE_RELATIVE_BLOCKS, TAPE_SPACE_SEQUENTIAL_FMKS, TAPE_SPACE_SEQUENTIAL_SMKS, TAPE_SPACE_SETMARKS, _win32_settapeposition, backup.settapeposition, base.settapeposition, winbase/SetTapePosition
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetTapePosition
 - winbase/SetTapePosition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - SetTapePosition
---

# SetTapePosition function


## -description

The 
<b>SetTapePosition</b> function sets the tape position on the specified device.

## -parameters

### -param hDevice [in]

Handle to the device on which to set the tape position. This handle is created by using the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.

### -param dwPositionMethod [in]

Type of positioning to perform. This parameter must be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TAPE_ABSOLUTE_BLOCK"></a><a id="tape_absolute_block"></a><dl>
<dt><b>TAPE_ABSOLUTE_BLOCK</b></dt>
<dt>1L</dt>
</dl>
</td>
<td width="60%">
Moves the tape to the device-specific block address specified by the <i>dwOffsetLow</i> and <i>dwOffsetHigh</i> parameters. The <i>dwPartition</i> parameter is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_LOGICAL_BLOCK"></a><a id="tape_logical_block"></a><dl>
<dt><b>TAPE_LOGICAL_BLOCK</b></dt>
<dt>2L</dt>
</dl>
</td>
<td width="60%">
Moves the tape to the block address specified by <i>dwOffsetLow</i> and <i>dwOffsetHigh</i> in the partition specified by <i>dwPartition</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_REWIND"></a><a id="tape_rewind"></a><dl>
<dt><b>TAPE_REWIND</b></dt>
<dt>0L</dt>
</dl>
</td>
<td width="60%">
Moves the tape to the beginning of the current partition. The <i>dwPartition</i>, <i>dwOffsetLow</i>, and <i>dwOffsetHigh</i> parameters are ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_SPACE_END_OF_DATA"></a><a id="tape_space_end_of_data"></a><dl>
<dt><b>TAPE_SPACE_END_OF_DATA</b></dt>
<dt>4L</dt>
</dl>
</td>
<td width="60%">
Moves the tape to the end of the data on the partition specified by <i>dwPartition</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_SPACE_FILEMARKS"></a><a id="tape_space_filemarks"></a><dl>
<dt><b>TAPE_SPACE_FILEMARKS</b></dt>
<dt>6L</dt>
</dl>
</td>
<td width="60%">
Moves the tape forward (or backward) the number of filemarks specified by <i>dwOffsetLow</i> and <i>dwOffsetHigh</i> in the current partition. The <i>dwPartition</i> parameter is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_SPACE_RELATIVE_BLOCKS"></a><a id="tape_space_relative_blocks"></a><dl>
<dt><b>TAPE_SPACE_RELATIVE_BLOCKS</b></dt>
<dt>5L</dt>
</dl>
</td>
<td width="60%">
Moves the tape forward (or backward) the number of blocks specified by <i>dwOffsetLow</i> and <i>dwOffsetHigh</i> in the current partition. The <i>dwPartition</i> parameter is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_SPACE_SEQUENTIAL_FMKS"></a><a id="tape_space_sequential_fmks"></a><dl>
<dt><b>TAPE_SPACE_SEQUENTIAL_FMKS</b></dt>
<dt>7L</dt>
</dl>
</td>
<td width="60%">
Moves the tape forward (or backward) to the first occurrence of n filemarks in the current partition, where n is the number specified by <i>dwOffsetLow</i> and <i>dwOffsetHigh</i>. The <i>dwPartition</i> parameter is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_SPACE_SEQUENTIAL_SMKS"></a><a id="tape_space_sequential_smks"></a><dl>
<dt><b>TAPE_SPACE_SEQUENTIAL_SMKS</b></dt>
<dt>9L</dt>
</dl>
</td>
<td width="60%">
Moves the tape forward (or backward) to the first occurrence of n setmarks in the current partition, where n is the number specified by <i>dwOffsetLow</i> and <i>dwOffsetHigh</i>. The <i>dwPartition</i> parameter is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_SPACE_SETMARKS"></a><a id="tape_space_setmarks"></a><dl>
<dt><b>TAPE_SPACE_SETMARKS</b></dt>
<dt>8L</dt>
</dl>
</td>
<td width="60%">
Moves the tape forward (or backward) the number of setmarks specified by <i>dwOffsetLow</i> and <i>dwOffsetHigh</i> in the current partition. The <i>dwPartition</i> parameter is ignored.

</td>
</tr>
</table>

### -param dwPartition [in]

Partition to position within. If <i>dwPartition</i> is zero, the current partition is used. Partitions are numbered logically from 1 through n, where 1 is the first partition on the tape and n is the last.

### -param dwOffsetLow [in]

Low-order bits of the block address or count for the position operation specified by the <i>dwPositionMethod</i> parameter.

### -param dwOffsetHigh [in]

High-order bits of the block address or count for the position operation specified by the <i>dwPositionMethod</i> parameter. If the high-order bits are not required, this parameter should be zero.

### -param bImmediate [in]

Indicates whether to return as soon as the move operation begins. If this parameter is <b>TRUE</b>, the function returns immediately; if <b>FALSE</b>, the function does not return until the move operation has been completed.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, it can return one of the following error codes.

<table>
<tr>
<th>Error</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BEGINNING_OF_MEDIA</b></dt>
<dt>1102L</dt>
</dl>
</td>
<td width="60%">
An attempt to access data before the beginning-of-medium marker failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUS_RESET</b></dt>
<dt>1111L</dt>
</dl>
</td>
<td width="60%">
A reset condition was detected on the bus.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DEVICE_NOT_PARTITIONED</b></dt>
<dt>1107L</dt>
</dl>
</td>
<td width="60%">
The partition information could not be found when a tape was being loaded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_END_OF_MEDIA</b></dt>
<dt>1100L</dt>
</dl>
</td>
<td width="60%">
The end-of-tape marker was reached during an operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILEMARK_DETECTED</b></dt>
<dt>1101L</dt>
</dl>
</td>
<td width="60%">
A filemark was reached during an operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_BLOCK_LENGTH</b></dt>
<dt>1106L</dt>
</dl>
</td>
<td width="60%">
The block size is incorrect on a new tape in a multivolume partition.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MEDIA_CHANGED</b></dt>
<dt>1110L</dt>
</dl>
</td>
<td width="60%">
The tape that was in the drive has been replaced or removed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_DATA_DETECTED</b></dt>
<dt>1104L</dt>
</dl>
</td>
<td width="60%">
The end-of-data marker was reached during an operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MEDIA_IN_DRIVE</b></dt>
<dt>1112L</dt>
</dl>
</td>
<td width="60%">
There is no media in the drive.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
<dt>50L</dt>
</dl>
</td>
<td width="60%">
The tape driver does not support a requested function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PARTITION_FAILURE</b></dt>
<dt>1105L</dt>
</dl>
</td>
<td width="60%">
The tape could not be partitioned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SETMARK_DETECTED</b></dt>
<dt>1103L</dt>
</dl>
</td>
<td width="60%">
A setmark was reached during an operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNABLE_TO_LOCK_MEDIA</b></dt>
<dt>1108L</dt>
</dl>
</td>
<td width="60%">
An attempt to lock the ejection mechanism failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNABLE_TO_UNLOAD_MEDIA</b></dt>
<dt>1109L</dt>
</dl>
</td>
<td width="60%">
An attempt to unload the tape failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WRITE_PROTECT</b></dt>
<dt>19L</dt>
</dl>
</td>
<td width="60%">
The media is write protected.

</td>
</tr>
</table>

## -remarks

If the offset specified by <i>dwOffsetLow</i> and <i>dwOffsetHigh</i> specifies the number of blocks, filemarks, or setmarks to move, a positive offset moves the tape forward to the end of the last block, filemark, or setmark. A negative offset moves the tape backward to the beginning of the last block, filemark, or setmark. If the offset is zero, the tape does not move.

To obtain information about the status, capabilities, and capacities of tape drives and media, call the 
<a href="/windows/desktop/api/winbase/nf-winbase-gettapeparameters">GetTapeParameters</a> function.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-gettapeparameters">GetTapeParameters</a>



<a href="/windows/desktop/api/winbase/nf-winbase-gettapeposition">GetTapePosition</a>