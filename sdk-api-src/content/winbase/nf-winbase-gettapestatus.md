---
UID: NF:winbase.GetTapeStatus
title: GetTapeStatus function (winbase.h)
description: Determines whether the tape device is ready to process tape commands.
helpviewer_keywords: ["GetTapeStatus","GetTapeStatus function [Backup]","_win32_gettapestatus","backup.gettapestatus","base.gettapestatus","winbase/GetTapeStatus"]
old-location: backup\gettapestatus.htm
tech.root: Backup
ms.assetid: 37422a27-2d46-43db-9318-4a3547b7f933
ms.date: 12/05/2018
ms.keywords: GetTapeStatus, GetTapeStatus function [Backup], _win32_gettapestatus, backup.gettapestatus, base.gettapestatus, winbase/GetTapeStatus
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
 - GetTapeStatus
 - winbase/GetTapeStatus
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
 - GetTapeStatus
---

# GetTapeStatus function


## -description

The 
<b>GetTapeStatus</b> function determines whether the tape device is ready to process tape commands.

## -parameters

### -param hDevice [in]

Handle to the device for which to get the device status. This handle is created by using the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.

## -returns

If the tape device is ready to accept appropriate tape-access commands without returning errors, the return value is NO_ERROR.

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
<dt><b>ERROR_DEVICE_REQUIRES_CLEANING</b></dt>
<dt>1165L</dt>
</dl>
</td>
<td width="60%">
The tape drive is capable of reporting that it requires cleaning, and reports that it does require cleaning.

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

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>