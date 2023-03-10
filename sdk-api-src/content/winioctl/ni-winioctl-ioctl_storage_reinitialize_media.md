---
UID: NI:winioctl.IOCTL_STORAGE_REINITIALIZE_MEDIA
title: IOCTL_STORAGE_REINITIALIZE_MEDIA
description: The IOCTL_STORAGE_REINITIALIZE_MEDIA ioctl (winioctl.h) offloads the erasure process to the storage device.
ms.date: 08/09/2022
ms.keywords: IOCTL_STORAGE_REINITIALIZE_MEDIA
targetos: Windows
req.construct-type: ioctl
req.ddi-compliance: 
req.dll: 
req.header: winioctl.h
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
f1_keywords:
 - IOCTL_STORAGE_REINITIALIZE_MEDIA
 - winioctl/IOCTL_STORAGE_REINITIALIZE_MEDIA
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winioctl.h
api_name:
 - IOCTL_STORAGE_REINITIALIZE_MEDIA
---

## -description

This IOCTL offloads the erasure process to the storage device.

## -ioctlparameters

### -input-buffer

### -input-buffer-length

### -output-buffer

### -output-buffer-length

### -in-out-buffer

### -inout-buffer-length

### -status-block

## -remarks

There is no guarantee as to the successful deletion or recoverability of the data on the storage device after command completion. This IOCTL is limited to data disks in regular Windows. In WinPE, this IOCTL is supported for both boot and data disks.

There may be cached data from the storage device in the system. To ensure there is no cached data from the storage device before erasure, call FSCTL_LOCK_VOLUME. The operating system does not ensure all outstanding requests to the storage device are completed before issuing the erasure command to the device.

## -see-also

