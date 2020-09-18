---
UID: NF:virtdisk.RawSCSIVirtualDisk
title: RawSCSIVirtualDisk function (virtdisk.h)
description: Issues an embedded SCSI request directly to a virtual hard disk.
helpviewer_keywords: ["RawSCSIVirtualDisk","RawSCSIVirtualDisk function [VHD]","vdssys/RawSCSIVirtualDisk","vhd.rawscsivirtualdisk","virtdisk/RawSCSIVirtualDisk"]
old-location: vhd\rawscsivirtualdisk.htm
tech.root: VStor
ms.assetid: AB766EC7-2D6E-44EB-9C5C-C840A77242CE
ms.date: 12/05/2018
ms.keywords: RawSCSIVirtualDisk, RawSCSIVirtualDisk function [VHD], vdssys/RawSCSIVirtualDisk, vhd.rawscsivirtualdisk, virtdisk/RawSCSIVirtualDisk
req.header: virtdisk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
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
req.lib: VirtDisk.lib
req.dll: VirtDisk.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RawSCSIVirtualDisk
 - virtdisk/RawSCSIVirtualDisk
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - VirtDisk.dll
api_name:
 - RawSCSIVirtualDisk
---

# RawSCSIVirtualDisk function


## -description

Issues an embedded SCSI request directly to a virtual hard disk.

## -parameters

### -param VirtualDiskHandle [in]

A handle to an open virtual disk. For information on how to open a virtual disk, see the 
      <a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk">OpenVirtualDisk</a> function. This handle may also be a handle to a Remote Shared Virtual Disk. For information on how to open a Remote Shared Virtual Disk, see the <a href="/openspecs/windows_protocols/ms-rsvd/c865c326-47d6-4a91-a62d-0e8f26007d15">Remote Shared Virtual Disk Protocol</a> documentation.

### -param Parameters [in]

A pointer to a valid <a href="/windows/win32/api/virtdisk/ns-virtdisk-raw_scsi_virtual_disk_parameters">RAW_SCSI_VIRTUAL_DISK_PARAMETERS</a> structure that contains snapshot deletion data.

### -param Flags [in]

SCSI virtual disk flags, which must be a valid combination of the <a href="/windows/win32/api/virtdisk/ne-virtdisk-raw_scsi_virtual_disk_flag">RAW_SCSI_VIRTUAL_DISK_FLAG</a> enumeration.

### -param Response [out]

A pointer to a <a href="/windows/win32/api/virtdisk/ns-virtdisk-raw_scsi_virtual_disk_response">RAW_SCSI_VIRTUAL_DISK_RESPONSE</a> structure that contains the results of processing the SCSI command.

## -returns

Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. 

A return of <b>ERROR_SUCCESS</b> only means the request was received by the virtual disk. The SCSI command itself could have failed due to an invalid device state, an unsupported SCSI command, or another error.

If the function fails, the return value is an error code. For more information, see 
       <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.