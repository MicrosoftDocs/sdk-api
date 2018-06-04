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
 

 

