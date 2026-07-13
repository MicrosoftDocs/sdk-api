---
UID: NS:emi.EMI_VERSION
title: EMI_VERSION (emi.h)
description: The EMI_VERSION structure describes the version of the Energy Metering Interface (EMI) that is supported by a device.
helpviewer_keywords: ["EMI_VERSION","EMI_VERSION structure [Power Metering and Budgeting Devices]","PEMI_VERSION","PEMI_VERSION structure pointer [Power Metering and Budgeting Devices]","emi/EMI_VERSION","emi/PEMI_VERSION","powermeter.emi_version"]
old-location: powermeter\emi_version.htm
tech.root: powermeter
ms.assetid: 00CDB74C-B0DB-426E-9D94-7DBCFF15793F
ms.date: 12/05/2018
ms.keywords: EMI_VERSION, EMI_VERSION structure [Power Metering and Budgeting Devices], PEMI_VERSION, PEMI_VERSION structure pointer [Power Metering and Budgeting Devices], emi/EMI_VERSION, emi/PEMI_VERSION, powermeter.emi_version
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
req.typenames: EMI_VERSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EMI_VERSION
 - emi/EMI_VERSION
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
 - EMI_VERSION
---

# EMI_VERSION structure


## -description

The <b>EMI_VERSION</b> structure describes the version of the Energy Metering Interface (EMI) that is supported by a device.

## -struct-fields

### -field EmiVersion

The version of the Energy Metering Interface (EMI) that is supported by a device. Currently, the only supported version is <b>EMI_VERSION_V1</b> (as defined in emi.h).

## -remarks

This structure is returned through a successful completion of an <a href="/windows/desktop/api/emi/ni-emi-ioctl_emi_get_version">IOCTL_EMI_GET_VERSION</a> IOCTL request.

## -see-also

<a href="/windows-hardware/drivers/powermeter/energy-meter-interface">Energy Metering Interface</a>



<a href="/windows/desktop/api/emi/ni-emi-ioctl_emi_get_version">IOCTL_EMI_GET_VERSION</a>

