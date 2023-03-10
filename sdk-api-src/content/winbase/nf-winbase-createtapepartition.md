---
UID: NF:winbase.CreateTapePartition
title: CreateTapePartition function (winbase.h)
description: Reformats a tape.
helpviewer_keywords: ["CreateTapePartition","CreateTapePartition function [Backup]","TAPE_FIXED_PARTITIONS","TAPE_INITIATOR_PARTITIONS","TAPE_SELECT_PARTITIONS","_win32_createtapepartition","backup.createtapepartition","base.createtapepartition","winbase/CreateTapePartition"]
old-location: backup\createtapepartition.htm
tech.root: Backup
ms.assetid: 9add07a2-1f70-4c9a-b278-4bc8b6c9d043
ms.date: 12/05/2018
ms.keywords: CreateTapePartition, CreateTapePartition function [Backup], TAPE_FIXED_PARTITIONS, TAPE_INITIATOR_PARTITIONS, TAPE_SELECT_PARTITIONS, _win32_createtapepartition, backup.createtapepartition, base.createtapepartition, winbase/CreateTapePartition
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
 - CreateTapePartition
 - winbase/CreateTapePartition
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
 - CreateTapePartition
---

# CreateTapePartition function


## -description

The 
<b>CreateTapePartition</b> function reformats a tape.

## -parameters

### -param hDevice [in]

Handle to the device where the new partition is to be created. This handle is created by using the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.

### -param dwPartitionMethod [in]

Type of partition to create. To determine what type of partitions your device supports, see the documentation for your hardware. This parameter can have one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TAPE_FIXED_PARTITIONS"></a><a id="tape_fixed_partitions"></a><dl>
<dt><b>TAPE_FIXED_PARTITIONS</b></dt>
<dt>0L</dt>
</dl>
</td>
<td width="60%">
Partitions the tape based on the device's default definition of partitions. The <i>dwCount</i> and <i>dwSize</i> parameters are ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_INITIATOR_PARTITIONS"></a><a id="tape_initiator_partitions"></a><dl>
<dt><b>TAPE_INITIATOR_PARTITIONS</b></dt>
<dt>2L</dt>
</dl>
</td>
<td width="60%">
Partitions the tape into the number and size of partitions specified by <i>dwCount</i> and <i>dwSize</i>, respectively, except for the last partition. The size of the last partition is the remainder of the tape.

</td>
</tr>
<tr>
<td width="40%"><a id="TAPE_SELECT_PARTITIONS"></a><a id="tape_select_partitions"></a><dl>
<dt><b>TAPE_SELECT_PARTITIONS</b></dt>
<dt>1L</dt>
</dl>
</td>
<td width="60%">
Partitions the tape into the number of partitions specified by <i>dwCount</i>. The <i>dwSize</i> parameter is ignored. The size of the partitions is determined by the device's default partition size. For more specific information, see the documentation for your tape device.

</td>
</tr>
</table>

### -param dwCount [in]

Number of partitions to create. The 
<a href="/windows/desktop/api/winbase/nf-winbase-gettapeparameters">GetTapeParameters</a> function provides the maximum number of partitions a tape can support.

### -param dwSize [in]

Size of each partition, in megabytes. This value is ignored if the <i>dwPartitionMethod</i> parameter is <b>TAPE_SELECT_PARTITIONS</b>.

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

Creating partitions reformats the tape. All previous information recorded on the tape is destroyed.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-gettapeparameters">GetTapeParameters</a>