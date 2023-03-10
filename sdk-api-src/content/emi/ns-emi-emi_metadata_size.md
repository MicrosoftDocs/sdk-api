---
UID: NS:emi.EMI_METADATA_SIZE
title: EMI_METADATA_SIZE (emi.h)
description: The EMI_METADATA_SIZE structure specifies the size of the Energy Metering Interface (EMI) metadata object that can be obtained from the device by issuing an IOCTL_EMI_GET_METADATA request.
helpviewer_keywords: ["EMI_METADATA_SIZE","EMI_METADATA_SIZE structure [Power Metering and Budgeting Devices]","PEMI_METADATA_SIZE","PEMI_METADATA_SIZE structure pointer [Power Metering and Budgeting Devices]","emi/EMI_METADATA_SIZE","emi/PEMI_METADATA_SIZE","powermeter.emi_metadata_size"]
old-location: powermeter\emi_metadata_size.htm
tech.root: powermeter
ms.assetid: EC9C71E8-7864-464B-8F16-E9D80460B36B
ms.date: 12/05/2018
ms.keywords: EMI_METADATA_SIZE, EMI_METADATA_SIZE structure [Power Metering and Budgeting Devices], PEMI_METADATA_SIZE, PEMI_METADATA_SIZE structure pointer [Power Metering and Budgeting Devices], emi/EMI_METADATA_SIZE, emi/PEMI_METADATA_SIZE, powermeter.emi_metadata_size
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
req.typenames: EMI_METADATA_SIZE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EMI_METADATA_SIZE
 - emi/EMI_METADATA_SIZE
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
 - EMI_METADATA_SIZE
---

# EMI_METADATA_SIZE structure


## -description

The <b>EMI_METADATA_SIZE</b> structure specifies the size of the  Energy Metering Interface (EMI) metadata object that can be obtained from the device by issuing an <a href="/windows/desktop/api/emi/ni-emi-ioctl_emi_get_metadata">IOCTL_EMI_GET_METADATA</a> request.

## -struct-fields

### -field MetadataSize

The size of the  EMI metadata (an [EMI_METADATA](./ns-emi-emi_metadata_v1.md) structure) that can be obtained from the device.

## -remarks

This structure is returned through a successful completion of an <a href="/windows/desktop/api/emi/ni-emi-ioctl_emi_get_metadata_size">IOCTL_EMI_GET_METADATA_SIZE</a> IOCTL request.

## -see-also

<a href="/windows-hardware/drivers/powermeter/energy-meter-interface">Energy Metering Interface</a>



<a href="/windows/desktop/api/emi/ni-emi-ioctl_emi_get_metadata_size">IOCTL_EMI_GET_METADATA_SIZE</a>

