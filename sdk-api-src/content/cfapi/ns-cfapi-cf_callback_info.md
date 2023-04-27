---
UID: NS:cfapi.CF_CALLBACK_INFO
title: CF_CALLBACK_INFO (cfapi.h)
description: Contains common callback information.
helpviewer_keywords: ["CF_CALLBACK_INFO","CF_CALLBACK_INFO structure","cfapi/CF_CALLBACK_INFO","cloudApi.cf_callback_info"]
old-location: cloudapi\cf_callback_info.htm
tech.root: cloudapi
ms.assetid: EF24E61E-4AF7-4946-A326-1F045267AE01
ms.date: 04/04/2023
ms.keywords: CF_CALLBACK_INFO, CF_CALLBACK_INFO structure, cfapi/CF_CALLBACK_INFO, cloudApi.cf_callback_info
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CF_CALLBACK_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_CALLBACK_INFO
 - cfapi/CF_CALLBACK_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_CALLBACK_INFO
---

## -description

Contains common callback information such as the callback type, the user process that triggers the callback, and the basic information about the file on which the callback is requested.

## -struct-fields

### -field StructSize

The size of **CF_CALLBACK_INFO**.

### -field ConnectionKey

An opaque handle created by [CfConnectSyncRoot](nf-cfapi-cfconnectsyncroot.md) for a sync root managed by the sync provider. *ConnectionKey* is returned as a convenience so the sync provider doesn't need to manually track it.

### -field CallbackContext

Points to an opaque blob that the sync provider provides at the sync root connect time. *CallbackContext* is returned as a convenience so the sync provider doesn't need to manually track it.

### -field VolumeGuidName

GUID name of the volume on which the placeholder file/directory to be serviced resides. It is in the form: “\\?\Volume{GUID}”.

### -field VolumeDosName

DOS drive letter of the volume in the form of "X:" where **X** is the drive letter.

### -field VolumeSerialNumber

The serial number of the volume.

### -field SyncRootFileId

A 64 bit file system maintained, volume-wide unique ID of the sync root under which the placeholder file or directory to be serviced resides.

### -field SyncRootIdentity

Points to the opaque blob provided by the sync provider at the sync root registration time.

### -field SyncRootIdentityLength

The length, in bytes, of the *SyncRootIdentity*.

### -field FileId

A 64 bit file system maintained, volume-wide unique ID of the placeholder file or directory to be serviced.

### -field FileSize

The logical size of the placeholder file to be serviced. It is always `0` if the subject of the callback is a directory.

### -field FileIdentity

Points to the opaque blob that the sync provider provides at the placeholder creation/conversion/update time.

### -field FileIdentityLength

The length, in bytes, of *FileIdentity*.

### -field NormalizedPath

The absolute path of the placeholder file or directory to be serviced on the volume identified by VolumeGuidName/VolumeDosName. It starts from the root directory of the volume. See the [Remarks](#-remarks) section for more details.

### -field TransferKey

An opaque handle to the placeholder file/directory to be serviced. The sync provider must pass it back to the [CfExecute](nf-cfapi-cfexecute.md) call in order to perform the desired operation on the file/directory.

### -field PriorityHint

A numeric scale given to the sync provider to describe the relative priority of one fetch compared to another fetch, in order to provide the most responsive experience to the user. The values range from `0` (lowest possible priority) to `15` (highest possible priority), but otherwise the values have no specific meaning. The filter may adjust how it chooses priority hints according to conditions. The sync provider is free to use the hint however it chooses.

### -field CorrelationVector

An optional correlation vector.

### -field ProcessInfo

Points to a [CF_PROCESS_INFO](ns-cfapi-cf_process_info.md) structure that contains the information about the user process that triggers this callback. It is present only if the sync provider specifies **CF_CONNECT_FLAG_REQUIRE_PROCESS_INFO** at the sync root connect time.

### -field RequestKey

An opaque id that uniquely identifies a cloud file operation on a particular cloud file as indicated by *TransferKey*. Sync providers don’t need to interpret this field. The only requirement on a sync provider is to transfer it as-is to [CF_OPERATION_INFO](ns-cfapi-cf_operation_info.md).

## -remarks

A file name is considered normalized if all of the following are true:

- It contains the full directory path for the file, including the volume name, unless the user opened the file by file ID but does not have traverse privilege for the entire path. (For more information, see [FltGetFileNameInformation](/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltgetfilenameinformation).)
- The volume name is the volume's non-persistent device object name (for example, "\Device\HarddiskVolume1").
- All short names are expanded to the equivalent long names.
- Any trailing ":$DATA" or "::$DATA" strings are removed from the stream name.
- All mount points are resolved.

## -see-also

[CfConnectSyncRoot](nf-cfapi-cfconnectsyncroot.md)

[CfExecute](nf-cfapi-cfexecute.md)

[CF_PROCESS_INFO](ns-cfapi-cf_process_info.md)

[CF_OPERATION_INFO](ns-cfapi-cf_operation_info.md)

[FltGetFileNameInformation](/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltgetfilenameinformation)
