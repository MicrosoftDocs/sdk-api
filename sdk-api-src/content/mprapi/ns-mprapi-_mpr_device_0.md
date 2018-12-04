---
UID: NS:mprapi._MPR_DEVICE_0
title: "_MPR_DEVICE_0"
author: windows-sdk-content
description: The MPR_DEVICE_0 structure stores information about a device used for a link in a multilinked demand dial interface.
old-location: rras\mpr_device_0.htm
tech.root: rras
ms.assetid: 1814c428-1a3c-45f3-8b15-182e1eceff7b
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: "*PMPR_DEVICE_0, MPR_DEVICE_0, MPR_DEVICE_0 structure [RAS], PMPR_DEVICE_0, PMPR_DEVICE_0 structure pointer [RAS], _MPR_DEVICE_0, _mpr_mpr_device_0, mprapi/MPR_DEVICE_0, mprapi/PMPR_DEVICE_0, rras.mpr_device_0"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - MPR_DEVICE_0
product: Windows
targetos: Windows
req.typenames: MPR_DEVICE_0, *PMPR_DEVICE_0
req.redist: 
---

# _MPR_DEVICE_0 structure


## -description


The 
<b>MPR_DEVICE_0</b> structure stores information about a device used for a link in a multilinked demand dial interface.


## -struct-fields




### -field szDeviceType

Specifies a null-terminated string that indicates the RAS device type referenced by <b>szDeviceName</b>. See 
<a href="https://msdn.microsoft.com/486f3526-2b0e-4f08-bb85-3aebf10cd52e">MPR_INTERFACE_2</a> for a list of possible device types.


### -field szDeviceName

Specifies a null-terminated string that contains the name of the TAPI device to use with this phone-book entry.


## -see-also




<a href="https://msdn.microsoft.com/99245e45-114d-4933-9189-cd45a1c22a96">MPR_DEVICE_1</a>



<a href="https://msdn.microsoft.com/edff88dd-80ae-4704-b320-925006346dda">MprAdminInterfaceDeviceGetInfo</a>



<a href="https://msdn.microsoft.com/ae8b3762-f176-4f91-97fc-33f7a9dcd424">MprAdminInterfaceDeviceSetInfo</a>
 

 

