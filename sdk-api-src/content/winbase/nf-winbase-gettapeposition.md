---
UID: NF:winbase.GetTapePosition
title: GetTapePosition function (winbase.h)
description: Retrieves the current address of the tape, in logical or absolute blocks.
helpviewer_keywords: ["GetTapePosition","GetTapePosition function [Backup]","TAPE_ABSOLUTE_POSITION","TAPE_LOGICAL_POSITION","_win32_gettapeposition","backup.gettapeposition","base.gettapeposition","winbase/GetTapePosition"]
old-location: backup\gettapeposition.htm
tech.root: Backup
ms.assetid: f4ce1436-ee16-4e05-b7a0-30ea79688e79
ms.date: 12/05/2018
ms.keywords: GetTapePosition, GetTapePosition function [Backup], TAPE_ABSOLUTE_POSITION, TAPE_LOGICAL_POSITION, _win32_gettapeposition, backup.gettapeposition, base.gettapeposition, winbase/GetTapePosition
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
 - GetTapePosition
 - winbase/GetTapePosition
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
 - GetTapePosition
---

# GetTapePosition function


## -description

The 
<b>GetTapePosition</b> function retrieves the current address of the tape, in logical or absolute blocks.

## -parameters

### -param hDevice [in]

Handle to the device on which to get the tape position. This handle is created by using 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>.

### -param dwPositionType [in]

Type of address to obtain. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TAPE_ABSOLUTE_POSITION"></a><a id="tape_absolute_position"></a><dl>
<dt><b>TAPE_ABSOLUTE_POSITION</b></dt>
<dt>0L</dt>
</dl>
</td>
<td width="60%">
The <i>lpdwOffsetLow</i> and <i>lpdwOffsetHigh</i> parameters receive the device-specific block address. The <i>dwPartition</i> parameter receives zero.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_LOGICAL_POSITION"></a><a id="tape_logical_position"></a><dl>
<dt><b>TAPE_LOGICAL_POSITION</b></dt>
<dt>1L</dt>
</dl>
</td>
<td width="60%">
The <i>lpdwOffsetLow</i> and <i>lpdwOffsetHigh</i> parameters receive the logical block address. The <i>dwPartition</i> parameter receives the logical tape partition.

</td>
</tr>
</table>

### -param lpdwPartition [out]

Pointer to a variable that receives the number of the current tape partition. Partitions are numbered logically from 1 through n, where 1 is the first partition on the tape and n is the last. When a device-specific block address is retrieved, or if the device supports only one partition, this parameter receives zero.

### -param lpdwOffsetLow [out]

Pointer to a variable that receives the low-order bits of the current tape position.

### -param lpdwOffsetHigh [out]

Pointer to a variable that receives the high-order bits of the current tape position. This parameter can be <b>NULL</b> if the high-order bits are not required.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, it can return one of the following error codes.

<table>
<tr>
<th>Error code</th>
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

A logical block address is relative to a partition. The first logical block address on each partition is zero.

Call the 
<a href="/windows/desktop/api/winbase/nf-winbase-gettapeparameters">GetTapeParameters</a> function to obtain information about the status, capabilities, and capacities of tape drives and media.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-gettapeparameters">GetTapeParameters</a>



<a href="/windows/desktop/api/winbase/nf-winbase-settapeposition">SetTapePosition</a>