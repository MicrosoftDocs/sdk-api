---
UID: NS:mprapi._MPR_DEVICE_1
title: "_MPR_DEVICE_1"
author: windows-sdk-content
description: The MPR_DEVICE_1 structure stores information about a device used for a link in a multilinked demand dial interface. In addition to the information in MPR_DEVICE_0, MPR_DEVICE_1 contains phone-number information.
old-location: rras\mpr_device_1.htm
old-project: rras
ms.assetid: 99245e45-114d-4933-9189-cd45a1c22a96
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: "*PMPR_DEVICE_1, MPR_DEVICE_1, MPR_DEVICE_1 structure [RAS], PMPR_DEVICE_1, PMPR_DEVICE_1 structure pointer [RAS], _MPR_DEVICE_1, _mpr_mpr_device_1, mprapi/MPR_DEVICE_1, mprapi/PMPR_DEVICE_1, rras.mpr_device_1"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: MPR_DEVICE_1, *PMPR_DEVICE_1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - MPR_DEVICE_1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MPR_DEVICE_1 structure


## -description


The 
<b>MPR_DEVICE_1</b> structure stores information about a device used for a link in a multilinked demand dial interface. In addition to the information in 
<a href="https://msdn.microsoft.com/1814c428-1a3c-45f3-8b15-182e1eceff7b">MPR_DEVICE_0</a>, 
<b>MPR_DEVICE_1</b> contains phone-number information.


## -struct-fields




### -field szDeviceType

Specifies a null-terminated string that indicates the device type referenced by <b>szDeviceName</b>. See 
<a href="https://msdn.microsoft.com/486f3526-2b0e-4f08-bb85-3aebf10cd52e">MPR_INTERFACE_2</a> for a list of possible device types.


### -field szDeviceName

Specifies a null-terminated string that contains the name of the TAPI device to use with this phone-book entry.


### -field szLocalPhoneNumber

Specifies a null-terminated Unicode string that contains a telephone number. The router uses the <b>szLocalPhoneNumber</b> string as the entire phone number.


### -field szAlternates

Pointer to a list of consecutive null-terminated Unicode strings. The last string is terminated by two consecutive null characters. The strings are alternate phone numbers that the router dials in the order listed if the primary number (see <b>szLocalPhoneNumber</b>) fails to connect.


## -see-also




<a href="https://msdn.microsoft.com/1814c428-1a3c-45f3-8b15-182e1eceff7b">MPR_DEVICE_0</a>



<a href="https://msdn.microsoft.com/edff88dd-80ae-4704-b320-925006346dda">MprAdminInterfaceDeviceGetInfo</a>



<a href="https://msdn.microsoft.com/ae8b3762-f176-4f91-97fc-33f7a9dcd424">MprAdminInterfaceDeviceSetInfo</a>
 

 

