---
UID: NI:emi.IOCTL_EMI_GET_VERSION
title: IOCTL_EMI_GET_VERSION (emi.h)
description: The IOCTL_EMI_GET_VERSION control code retrieves the current version of the EMI interface supported by the device.
helpviewer_keywords: ["IOCTL_EMI_GET_VERSION","IOCTL_EMI_GET_VERSION control","IOCTL_EMI_GET_VERSION control code [Power Metering and Budgeting Devices]","emi/IOCTL_EMI_GET_VERSION","powermeter.ioctl_emi_get_version"]
old-location: powermeter\ioctl_emi_get_version.htm
tech.root: powermeter
ms.assetid: 6B27B70C-DB3C-4EF9-B8FF-8074B0285F87
ms.date: 11/19/2021
ms.keywords: IOCTL_EMI_GET_VERSION, IOCTL_EMI_GET_VERSION control, IOCTL_EMI_GET_VERSION control code [Power Metering and Budgeting Devices], emi/IOCTL_EMI_GET_VERSION, powermeter.ioctl_emi_get_version
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
 - IOCTL_EMI_GET_VERSION
 - emi/IOCTL_EMI_GET_VERSION
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
 - IOCTL_EMI_GET_VERSION
---

# IOCTL_EMI_GET_VERSION IOCTL


## -description

The <b>IOCTL_EMI_GET_VERSION</b> 
   control code retrieves the current version of the EMI interface supported by the device.

## -ioctlparameters

### -input-buffer


<text> None. </text>

### -input-buffer-length

<text> None. </text>

### -output-buffer

<text> The <b> AssociatedIrp.SystemBuffer </b> member specifies the address of a caller-allocated buffer that contains a EMI_VERSION structure. On output, this structure holds the EMI version that is supported by the device. </text>

### -output-buffer-length

<text> The size of this buffer is specified in the <b> Parameters.DeviceIoControl.OutputBufferLength </b> member. </text>


### -status-block

Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

### -remarks

<b> EMI_VERSION_V1 </b> indicate there is only one single energy measurement channel supported by the device.
 
<b> EMI_VERSION_V2 </b> indicate there is multiple energy measurement channels supported by the device.

## -see-also

<a href="/windows-hardware/drivers/powermeter/energy-meter-interface">Energy Metering Interface</a>