---
UID: NS:mprapi._MPR_DEVICE_1
title: MPR_DEVICE_1 (mprapi.h)
description: The MPR_DEVICE_1 structure stores information about a device used for a link in a multilinked demand dial interface. In addition to the information in MPR_DEVICE_0, MPR_DEVICE_1 contains phone-number information.
helpviewer_keywords: ["*PMPR_DEVICE_1","MPR_DEVICE_1","MPR_DEVICE_1 structure [RAS]","PMPR_DEVICE_1","PMPR_DEVICE_1 structure pointer [RAS]","_mpr_mpr_device_1","mprapi/MPR_DEVICE_1","mprapi/PMPR_DEVICE_1","rras.mpr_device_1"]
old-location: rras\mpr_device_1.htm
tech.root: RRAS
ms.assetid: 99245e45-114d-4933-9189-cd45a1c22a96
ms.date: 12/05/2018
ms.keywords: '*PMPR_DEVICE_1, MPR_DEVICE_1, MPR_DEVICE_1 structure [RAS], PMPR_DEVICE_1, PMPR_DEVICE_1 structure pointer [RAS], _mpr_mpr_device_1, mprapi/MPR_DEVICE_1, mprapi/PMPR_DEVICE_1, rras.mpr_device_1'
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
req.typenames: MPR_DEVICE_1, *PMPR_DEVICE_1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MPR_DEVICE_1
 - mprapi/_MPR_DEVICE_1
 - PMPR_DEVICE_1
 - mprapi/PMPR_DEVICE_1
 - MPR_DEVICE_1
 - mprapi/MPR_DEVICE_1
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
 - MPR_DEVICE_1
---

# MPR_DEVICE_1 structure


## -description

The 
<b>MPR_DEVICE_1</b> structure stores information about a device used for a link in a multilinked demand dial interface. In addition to the information in 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_device_0">MPR_DEVICE_0</a>, 
<b>MPR_DEVICE_1</b> contains phone-number information.

## -struct-fields

### -field szDeviceType

Specifies a null-terminated string that indicates the device type referenced by <b>szDeviceName</b>. See 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_interface_2">MPR_INTERFACE_2</a> for a list of possible device types.

### -field szDeviceName

Specifies a null-terminated string that contains the name of the TAPI device to use with this phone-book entry.

### -field szLocalPhoneNumber

Specifies a null-terminated Unicode string that contains a telephone number. The router uses the <b>szLocalPhoneNumber</b> string as the entire phone number.

### -field szAlternates

Pointer to a list of consecutive null-terminated Unicode strings. The last string is terminated by two consecutive null characters. The strings are alternate phone numbers that the router dials in the order listed if the primary number (see <b>szLocalPhoneNumber</b>) fails to connect.

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_device_0">MPR_DEVICE_0</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacedevicegetinfo">MprAdminInterfaceDeviceGetInfo</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacedevicesetinfo">MprAdminInterfaceDeviceSetInfo</a>