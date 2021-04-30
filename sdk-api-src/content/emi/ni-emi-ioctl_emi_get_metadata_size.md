---
UID: NI:emi.IOCTL_EMI_GET_METADATA_SIZE
title: IOCTL_EMI_GET_METADATA_SIZE (emi.h)
description: The IOCTL_EMI_GET_METADATA_SIZE control code retrieves the size of the EMI metadata object that can be obtained from the device by issuing an IOCTL_EMI_GET_METADATA request.
helpviewer_keywords: ["IOCTL_EMI_GET_METADATA_SIZE","IOCTL_EMI_GET_METADATA_SIZE control","IOCTL_EMI_GET_METADATA_SIZE control code [Power Metering and Budgeting Devices]","emi/IOCTL_EMI_GET_METADATA_SIZE","powermeter.ioctl_emi_get_metadata_size"]
old-location: powermeter\ioctl_emi_get_metadata_size.htm
tech.root: powermeter
ms.assetid: 7A3E5BE5-F567-408A-B4AC-347E052957D9
ms.date: 12/05/2018
ms.keywords: IOCTL_EMI_GET_METADATA_SIZE, IOCTL_EMI_GET_METADATA_SIZE control, IOCTL_EMI_GET_METADATA_SIZE control code [Power Metering and Budgeting Devices], emi/IOCTL_EMI_GET_METADATA_SIZE, powermeter.ioctl_emi_get_metadata_size
req.header: emi.h
req.include-header: Emi.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows 10.
req.target-min-winversvr: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOCTL_EMI_GET_METADATA_SIZE
 - emi/IOCTL_EMI_GET_METADATA_SIZE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - emi.h
api_name:
 - IOCTL_EMI_GET_METADATA_SIZE
---

# IOCTL_EMI_GET_METADATA_SIZE IOCTL


## -description

The <b>IOCTL_EMI_GET_METADATA_SIZE</b> 
   control code retrieves the size of the  EMI metadata object that can be obtained from the device by issuing an <a href="/windows/desktop/api/emi/ni-emi-ioctl_emi_get_metadata">IOCTL_EMI_GET_METADATA</a> request.

## -ioctlparameters

### -input-buffer

<text></text>

### -input-buffer-length

<text></text>

### -output-buffer

<text></text>

### -output-buffer-length

<text></text>

### -in-out-buffer

<text></text>

### -inout-buffer-length

<text></text>

### -status-block

Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

## -see-also

<a href="/windows-hardware/drivers/powermeter/energy-meter-interface">Energy Metering Interface</a>