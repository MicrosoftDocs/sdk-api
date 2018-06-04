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

# _BLUETOOTH_COD_PAIRS structure


## -description


The 
<b>BLUETOOTH_COD_PAIRS</b> structure provides for specification and retrieval of Bluetooth Class Of Device (COD) information.


## -struct-fields




### -field ulCODMask

A mask to compare to determine the class of device. The major and minor codes of <b>ulCODMask</b> are used to compare  the class of device found.  If a major code is provided  it must match the major code returned by the remote device, such that GET_COD_MAJOR(ulCODMask) is equal to GET_COD_MAJOR([class of device of the remote device]).


### -field pcszDescription

Descriptive string of the mask.


## -remarks



If a minor code is provided in <b>ulCODMask</b> it must also match the minor code returned by the remote device.  A major code must be set if a minor code is specified; zero is not a valid major code.

See the Bluetooth specification at 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84017">www.bluetooth.com</a> for Class Of Device information.




## -see-also




<a href="https://msdn.microsoft.com/34ab348b-ce5d-422a-9bec-adbefa4a5ea0">BLUETOOTH_SELECT_DEVICE_PARAMS </a>
 

 

