---
UID: NF:winbase.PrepareTape
title: PrepareTape function (winbase.h)
description: Prepares the tape to be accessed or removed.
helpviewer_keywords: ["PrepareTape","PrepareTape function [Backup]","TAPE_FORMAT","TAPE_LOAD","TAPE_LOCK","TAPE_TENSION","TAPE_UNLOAD","TAPE_UNLOCK","_win32_preparetape","backup.preparetape","base.preparetape","winbase/PrepareTape"]
old-location: backup\preparetape.htm
tech.root: Backup
ms.assetid: 13aacf38-b0ae-4f4d-ada9-42c61490be7e
ms.date: 12/05/2018
ms.keywords: PrepareTape, PrepareTape function [Backup], TAPE_FORMAT, TAPE_LOAD, TAPE_LOCK, TAPE_TENSION, TAPE_UNLOAD, TAPE_UNLOCK, _win32_preparetape, backup.preparetape, base.preparetape, winbase/PrepareTape
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
 - PrepareTape
 - winbase/PrepareTape
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
 - PrepareTape
---

# PrepareTape function


## -description

The 
<b>PrepareTape</b> function prepares the tape to be accessed or removed.

## -parameters

### -param hDevice [in]

Handle to the device preparing the tape. This handle is created by using the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.

### -param dwOperation [in]

Tape device preparation. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TAPE_FORMAT"></a><a id="tape_format"></a><dl>
<dt><b>TAPE_FORMAT</b></dt>
<dt>5L</dt>
</dl>
</td>
<td width="60%">
Performs a low-level format of the tape. Currently, only the QIC117 device supports this feature.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_LOAD"></a><a id="tape_load"></a><dl>
<dt><b>TAPE_LOAD</b></dt>
<dt>0L</dt>
</dl>
</td>
<td width="60%">
Loads the tape and moves the tape to the beginning.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_LOCK"></a><a id="tape_lock"></a><dl>
<dt><b>TAPE_LOCK</b></dt>
<dt>3L</dt>
</dl>
</td>
<td width="60%">
Locks the tape ejection mechanism so that the tape is not ejected accidentally.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_TENSION"></a><a id="tape_tension"></a><dl>
<dt><b>TAPE_TENSION</b></dt>
<dt>2L</dt>
</dl>
</td>
<td width="60%">
Adjusts the tension by moving the tape to the end of the tape and back to the beginning. This option is not supported by all devices. This value is ignored if it is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_UNLOAD"></a><a id="tape_unload"></a><dl>
<dt><b>TAPE_UNLOAD</b></dt>
<dt>1L</dt>
</dl>
</td>
<td width="60%">
Moves the tape to the beginning for removal from the device. After a successful unload operation, the device returns errors to applications that attempt to access the tape, until the tape is loaded again.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_UNLOCK"></a><a id="tape_unlock"></a><dl>
<dt><b>TAPE_UNLOCK</b></dt>
<dt>4L</dt>
</dl>
</td>
<td width="60%">
Unlocks the tape ejection mechanism.

</td>
</tr>
</table>

### -param bImmediate [in]

If this parameter is <b>TRUE</b>, the function returns immediately. If it is <b>FALSE</b>, the function does not return until the operation has been completed.

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

Some tape devices do not support certain tape operations. See your tape device documentation and use the 
<a href="/windows/desktop/api/winbase/nf-winbase-gettapeparameters">GetTapeParameters</a> function to determine your tape device's capabilities.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-gettapeparameters">GetTapeParameters</a>