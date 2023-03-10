---
UID: NF:winbase.WriteTapemark
title: WriteTapemark function (winbase.h)
description: Writes a specified number of filemarks, setmarks, short filemarks, or long filemarks to a tape device.
helpviewer_keywords: ["TAPE_FILEMARKS","TAPE_LONG_FILEMARKS","TAPE_SETMARKS","TAPE_SHORT_FILEMARKS","WriteTapemark","WriteTapemark function [Backup]","_win32_writetapemark","backup.writetapemark","base.writetapemark","winbase/WriteTapemark"]
old-location: backup\writetapemark.htm
tech.root: Backup
ms.assetid: 74effd3b-693d-4808-9d80-6c70e2aef7fb
ms.date: 12/05/2018
ms.keywords: TAPE_FILEMARKS, TAPE_LONG_FILEMARKS, TAPE_SETMARKS, TAPE_SHORT_FILEMARKS, WriteTapemark, WriteTapemark function [Backup], _win32_writetapemark, backup.writetapemark, base.writetapemark, winbase/WriteTapemark
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
 - WriteTapemark
 - winbase/WriteTapemark
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
 - WriteTapemark
---

# WriteTapemark function


## -description

The 
<b>WriteTapemark</b> function writes a specified number of filemarks, setmarks, short filemarks, or long filemarks to a tape device. These tapemarks divide a tape partition into smaller areas.

## -parameters

### -param hDevice [in]

Handle to the device on which to write tapemarks. This handle is created by using the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.

### -param dwTapemarkType [in]

Type of tapemarks to write. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TAPE_FILEMARKS"></a><a id="tape_filemarks"></a><dl>
<dt><b>TAPE_FILEMARKS</b></dt>
<dt>1L</dt>
</dl>
</td>
<td width="60%">
Writes the number of filemarks specified by the <i>dwTapemarkCount</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_LONG_FILEMARKS"></a><a id="tape_long_filemarks"></a><dl>
<dt><b>TAPE_LONG_FILEMARKS</b></dt>
<dt>3L</dt>
</dl>
</td>
<td width="60%">
Writes the number of long filemarks specified by <i>dwTapemarkCount</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_SETMARKS"></a><a id="tape_setmarks"></a><dl>
<dt><b>TAPE_SETMARKS</b></dt>
<dt>0L</dt>
</dl>
</td>
<td width="60%">
Writes the number of setmarks specified by <i>dwTapemarkCount</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_SHORT_FILEMARKS"></a><a id="tape_short_filemarks"></a><dl>
<dt><b>TAPE_SHORT_FILEMARKS</b></dt>
<dt>2L</dt>
</dl>
</td>
<td width="60%">
Writes the number of short filemarks specified by <i>dwTapemarkCount</i>.

</td>
</tr>
</table>

### -param dwTapemarkCount [in]

Number of tapemarks to write.

### -param bImmediate [in]

If this parameter is <b>TRUE</b>, the function returns immediately; if it is <b>FALSE</b>, the function does not return until the operation has been completed.

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

Filemarks, setmarks, short filemarks, and long filemarks are special recorded elements that denote the linear organization of the tape. None of these marks contain user data. Filemarks are the most general marks; setmarks provide a hierarchy not available with filemarks.

A short filemark contains a short erase gap that cannot be overwritten unless the write operation is performed from the beginning of the partition or from an earlier long filemark.

A long filemark contains a long erase gap that allows an application to position the tape at the beginning of the filemark and to overwrite the filemark and the erase gap.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>