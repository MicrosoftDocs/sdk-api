---
UID: NI:emi.IOCTL_EMI_GET_VERSION
title: IOCTL_EMI_GET_VERSION (emi.h)
description: The IOCTL_EMI_GET_VERSION control code retrieves the current version of the EMI interface supported by the device.
helpviewer_keywords: ["IOCTL_EMI_GET_VERSION","IOCTL_EMI_GET_VERSION control","IOCTL_EMI_GET_VERSION control code [Power Metering and Budgeting Devices]","emi/IOCTL_EMI_GET_VERSION","powermeter.ioctl_emi_get_version"]
old-location: powermeter\ioctl_emi_get_version.htm
tech.root: powermeter
ms.assetid: 6B27B70C-DB3C-4EF9-B8FF-8074B0285F87
ms.date: 12/05/2018
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


### -input-buffer-length


### -output-buffer


### -output-buffer-length


### -in-out-buffer


### -inout-buffer-length


### -status-block

Irp->IoStatus.Status is set to STATUS_SUCCESS if the request is successful.

Otherwise, Status to the appropriate error condition as a NTSTATUS code. 

For more information, see [NTSTATUS Values](/windows-hardware/drivers/kernel/ntstatus-values).

## -see-also

<a href="/windows-hardware/drivers/powermeter/energy-meter-interface">Energy Metering Interface</a>