---
UID: NF:winbase.GetTapeParameters
title: GetTapeParameters function (winbase.h)
description: Retrieves information that describes the tape or the tape drive.
helpviewer_keywords: ["GET_TAPE_DRIVE_INFORMATION","GET_TAPE_MEDIA_INFORMATION","GetTapeParameters","GetTapeParameters function [Backup]","_win32_gettapeparameters","backup.gettapeparameters","base.gettapeparameters","winbase/GetTapeParameters"]
old-location: backup\gettapeparameters.htm
tech.root: Backup
ms.assetid: 87e59e29-e174-4462-b692-512c3380eb4d
ms.date: 12/05/2018
ms.keywords: GET_TAPE_DRIVE_INFORMATION, GET_TAPE_MEDIA_INFORMATION, GetTapeParameters, GetTapeParameters function [Backup], _win32_gettapeparameters, backup.gettapeparameters, base.gettapeparameters, winbase/GetTapeParameters
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
 - GetTapeParameters
 - winbase/GetTapeParameters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetTapeParameters
---

# GetTapeParameters function


## -description

The 
<b>GetTapeParameters</b> function retrieves information that describes the tape or the tape drive.

## -parameters

### -param hDevice [in]

Handle to the device about which information is sought. This handle is created by using the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.

### -param dwOperation [in]

Type of information requested. This parameter must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GET_TAPE_DRIVE_INFORMATION"></a><a id="get_tape_drive_information"></a><dl>
<dt><b>GET_TAPE_DRIVE_INFORMATION</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Retrieves information about the tape device.

</td>
</tr>
<tr>
<td width="40%"><a id="GET_TAPE_MEDIA_INFORMATION"></a><a id="get_tape_media_information"></a><dl>
<dt><b>GET_TAPE_MEDIA_INFORMATION</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Retrieves information about the tape in the tape device.

</td>
</tr>
</table>

### -param lpdwSize [out]

Pointer to a variable that receives the size, in bytes, of the buffer specified by the <i>lpTapeInformation</i> parameter. If the buffer is too small, this parameter receives the required size.

### -param lpTapeInformation [out]

Pointer to a structure that contains the requested information. If the <i>dwOperation</i> parameter is <b>GET_TAPE_MEDIA_INFORMATION</b>, <i>lpTapeInformation</i> points to a 
<a href="/windows/desktop/api/winnt/ns-winnt-tape_get_media_parameters">TAPE_GET_MEDIA_PARAMETERS</a> structure.

If <i>dwOperation</i> is <b>GET_TAPE_DRIVE_INFORMATION</b>, <i>lpTapeInformation</i> points to a 
<a href="/windows/desktop/api/winnt/ns-winnt-tape_get_drive_parameters">TAPE_GET_DRIVE_PARAMETERS</a> structure.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

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

The block size range values (maximum and minimum) returned by the 
<b>GetTapeParameters</b> function called with the <i>dwOperation</i> parameter set to the <b>GET_TAPE_DRIVE_INFORMATION</b> value will indicate system limits, not drive limits. However, it is the tape drive device and the media present in the drive that determine the true block size limits. Thus, an application may not be able to set all the block sizes mentioned in the range obtained by specifying <b>GET_TAPE_DRIVE_INFORMATION</b> in <i>dwOperation</i>.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-settapeparameters">SetTapeParameters</a>



<a href="/windows/desktop/api/winnt/ns-winnt-tape_get_drive_parameters">TAPE_GET_DRIVE_PARAMETERS</a>



<a href="/windows/desktop/api/winnt/ns-winnt-tape_get_media_parameters">TAPE_GET_MEDIA_PARAMETERS</a>