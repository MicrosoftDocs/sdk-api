---
UID: NI:winioctl.IOCTL_STORAGE_REINITIALIZE_MEDIA
title: IOCTL_STORAGE_REINITIALIZE_MEDIA
ms.date: 4/26/2019
ms.keywords: IOCTL_STORAGE_REINITIALIZE_MEDIA
f1_keywords:
- IOCTL_STORAGE_REINITIALIZE_MEDIA
dev_langs:
- c++
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
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
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

## -input-buffer

## -input-buffer-length

## -output-buffer

## -output-buffer-length

## -in-out-buffer

## -inout-buffer-length

## -status-block

## -remarks

There is no guarantee as to the successful deletion or recoverability of the data on the storage device after command completion. This IOCTL is limited to data disks in regular Windows. In WinPE, this IOCTL is supported for both boot and data disks.

There may be cached data from the storage device in the system. To ensure there is no cached data from the storage device before erasure, call FSCTL_LOCK_VOLUME. The operating system does not ensure all outstanding requests to the storage device are completed before issuing the erasure command to the device.

## -see-also

