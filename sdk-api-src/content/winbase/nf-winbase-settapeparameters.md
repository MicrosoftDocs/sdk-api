---
UID: NF:winbase.SetTapeParameters
title: SetTapeParameters function
author: windows-sdk-content
description: Specifies the block size of a tape or configures the tape device.
old-location: backup\settapeparameters.htm
tech.root: Backup
ms.assetid: 2043249b-b4ff-4bdd-9e6e-13c432a183cb
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SET_TAPE_DRIVE_INFORMATION, SET_TAPE_MEDIA_INFORMATION, SetTapeParameters, SetTapeParameters function [Backup], _win32_settapeparameters, backup.settapeparameters, base.settapeparameters, winbase/SetTapeParameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - SetTapeParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SetTapeParameters
: 
---

# SetTapeParameters function


## -description


The 
<b>SetTapeParameters</b> function either specifies the block size of a tape or configures the tape device.


## -parameters




### -param hDevice [in]

Handle to the device for which to set configuration information. This handle is created by using the 
<a href="https://msdn.microsoft.com/en-us/library/Aa363858(v=VS.85).aspx">CreateFile</a> function.


### -param dwOperation [in]

Type of information to set. This parameter must be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SET_TAPE_DRIVE_INFORMATION"></a><a id="set_tape_drive_information"></a><dl>
<dt><b>SET_TAPE_DRIVE_INFORMATION</b></dt>
<dt>1L</dt>
</dl>
</td>
<td width="60%">
Sets the device-specific information specified by <i>lpTapeInformation</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="SET_TAPE_MEDIA_INFORMATION"></a><a id="set_tape_media_information"></a><dl>
<dt><b>SET_TAPE_MEDIA_INFORMATION</b></dt>
<dt>0L</dt>
</dl>
</td>
<td width="60%">
Sets the tape-specific information specified by the <i>lpTapeInformation</i> parameter.

</td>
</tr>
</table>
 


### -param lpTapeInformation [in]

Pointer to a structure that contains the information to set. If the <i>dwOperation</i> parameter is SET_TAPE_MEDIA_INFORMATION, <i>lpTapeInformation</i> points to a 
<a href="https://msdn.microsoft.com/20243a64-2644-4519-b746-ba33f0893e49">TAPE_SET_MEDIA_PARAMETERS</a> structure. 




If <i>dwOperation</i> is SET_TAPE_DRIVE_INFORMATION, <i>lpTapeInformation</i> points to a 
<a href="https://msdn.microsoft.com/5615e83a-99c0-4214-8621-7e0561512816">TAPE_SET_DRIVE_PARAMETERS</a> structure.


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
 




## -see-also




<a href="https://msdn.microsoft.com/87e59e29-e174-4462-b692-512c3380eb4d">GetTapeParameters</a>



<a href="https://msdn.microsoft.com/5615e83a-99c0-4214-8621-7e0561512816">TAPE_SET_DRIVE_PARAMETERS</a>



<a href="https://msdn.microsoft.com/20243a64-2644-4519-b746-ba33f0893e49">TAPE_SET_MEDIA_PARAMETERS</a>
 

 

