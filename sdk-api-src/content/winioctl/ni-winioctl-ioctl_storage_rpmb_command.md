---
UID: NI:winioctl.IOCTL_STORAGE_RPMB_COMMAND
title: IOCTL_STORAGE_RPMB_COMMAND
description: The IOCTL_STORAGE_RPMB_COMMAND ioctl (winioctl.h) sends an RPMB command to the underlying storage device.
ms.date: 08/09/2022
ms.keywords: IOCTL_STORAGE_RPMB_COMMAND
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
 - IOCTL_STORAGE_RPMB_COMMAND
 - winioctl/IOCTL_STORAGE_RPMB_COMMAND
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - winioctl.h
api_name:
 - IOCTL_STORAGE_RPMB_COMMAND
---

## -description

This IOCTL sends an RPMB command to the underlying storage device.

## -ioctlparameters

### -input-buffer

An array of STORAGE_RPMB_DATA_FRAME structures.

### -input-buffer-length

A multiple of sizeof(STORAGE_RPMB_DATA_FRAME). InputBufferLength / sizeof(STORAGE_RPMB_DATA_FRAME) indicates the number of input frames.

### -output-buffer

An array of STORAGE_RPMB_DATA_FRAME structures.

### -output-buffer-length

A multiple of sizeof(STORAGE_RPMB_DATA_FRAME). The number of frames included can be calculated by OutputBufferLength / sizeof(STORAGE_RPMB_DATA_FRAME)

### -in-out-buffer

### -inout-buffer-length

### -status-block

## -remarks

## -see-also

