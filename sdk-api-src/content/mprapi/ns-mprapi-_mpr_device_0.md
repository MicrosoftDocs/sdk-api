---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
 

 

