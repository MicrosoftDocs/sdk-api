---
UID: NS:mprapi._MPR_DEVICE_0
title: MPR_DEVICE_0 (mprapi.h)
description: The MPR_DEVICE_0 structure stores information about a device used for a link in a multilinked demand dial interface.
helpviewer_keywords: ["*PMPR_DEVICE_0","MPR_DEVICE_0","MPR_DEVICE_0 structure [RAS]","PMPR_DEVICE_0","PMPR_DEVICE_0 structure pointer [RAS]","_mpr_mpr_device_0","mprapi/MPR_DEVICE_0","mprapi/PMPR_DEVICE_0","rras.mpr_device_0"]
old-location: rras\mpr_device_0.htm
tech.root: RRAS
ms.assetid: 1814c428-1a3c-45f3-8b15-182e1eceff7b
ms.date: 12/05/2018
ms.keywords: '*PMPR_DEVICE_0, MPR_DEVICE_0, MPR_DEVICE_0 structure [RAS], PMPR_DEVICE_0, PMPR_DEVICE_0 structure pointer [RAS], _mpr_mpr_device_0, mprapi/MPR_DEVICE_0, mprapi/PMPR_DEVICE_0, rras.mpr_device_0'
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: MPR_DEVICE_0, *PMPR_DEVICE_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MPR_DEVICE_0
 - mprapi/_MPR_DEVICE_0
 - PMPR_DEVICE_0
 - mprapi/PMPR_DEVICE_0
 - MPR_DEVICE_0
 - mprapi/MPR_DEVICE_0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - MPR_DEVICE_0
---

# MPR_DEVICE_0 structure


## -description

The 
<b>MPR_DEVICE_0</b> structure stores information about a device used for a link in a multilinked demand dial interface.

## -struct-fields

### -field szDeviceType

Specifies a null-terminated string that indicates the RAS device type referenced by <b>szDeviceName</b>. See 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_2">MPR_INTERFACE_2</a> for a list of possible device types.

### -field szDeviceName

Specifies a null-terminated string that contains the name of the TAPI device to use with this phone-book entry.

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_device_1">MPR_DEVICE_1</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacedevicegetinfo">MprAdminInterfaceDeviceGetInfo</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacedevicesetinfo">MprAdminInterfaceDeviceSetInfo</a>