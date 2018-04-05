---
UID: NF:virtdisk.RawSCSIVirtualDisk
title: RawSCSIVirtualDisk function
author: windows-driver-content
description: Issues an embedded SCSI request directly to a virtual hard disk.
old-location: vhd\rawscsivirtualdisk.htm
old-project: VStor
ms.assetid: AB766EC7-2D6E-44EB-9C5C-C840A77242CE
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: RawSCSIVirtualDisk, RawSCSIVirtualDisk function [VHD], vhd.rawscsivirtualdisk, virtdisk/RawSCSIVirtualDisk
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: virtdisk.h
req.include-header: Windows.h
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
req.typenames: VIRTUAL_DISK_ACCESS_MASK, VIRTUAL_DISK_ACCESS_MASK
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	VirtDisk.dll
api_name:
-	RawSCSIVirtualDisk
product: Windows
targetos: Windows
req.lib: VirtDisk.lib
req.dll: VirtDisk.dll
req.irql: 
req.product: Windows UI
---

# RawSCSIVirtualDisk function


## -description


Issues an embedded SCSI request directly to a virtual hard disk. 



## -parameters




### -param VirtualDiskHandle [in]

A handle to an open virtual disk. For information on how to open a virtual disk, see the 
      <a href="https://msdn.microsoft.com/08e2a82d-9110-42b1-be09-dc5150da42f6">OpenVirtualDisk</a> function. This handle may also be a handle to a Remote Shared Virtual Disk. For information on how to open a Remote Shared Virtual Disk, see the <a href="https://msdn.microsoft.com/en-us/library/dn393384.aspx">Remote Shared Virtual Disk Protocol</a> documentation. 



### -param Parameters [in]

A pointer to a valid <a href="https://msdn.microsoft.com/E6E6BD59-F7BC-4523-B368-6EBE12285593">RAW_SCSI_VIRTUAL_DISK_PARAMETERS</a> structure that contains snapshot deletion data.


### -param Flags [in]

SCSI virtual disk flags, which must be a valid combination of the <a href="https://msdn.microsoft.com/7E90EA65-F0A1-44C5-9254-ABE89E1F35A5">RAW_SCSI_VIRTUAL_DISK_FLAG</a> enumeration.


### -param Response [out]

A pointer to a <a href="https://msdn.microsoft.com/CF3240A0-134B-4494-8451-7F8C6429D435">RAW_SCSI_VIRTUAL_DISK_RESPONSE</a> structure that contains the results of processing the SCSI command. 



## -returns



Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. 

A return of <b>ERROR_SUCCESS</b> only means the request was received by the virtual disk. The SCSI command itself could have failed due to an invalid device state, an unsupported SCSI command, or another error.

If the function fails, the return value is an error code. For more information, see 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.



