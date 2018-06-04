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

# EMI_VERSION structure


## -description


The <b>EMI_VERSION</b> structure describes the version of the Energy Metering Interface (EMI) that is supported by a device.


## -struct-fields




### -field EmiVersion

The version of the Energy Metering Interface (EMI) that is supported by a device. Currently, the only supported version is <b>EMI_VERSION_V1</b> (as defined in emi.h).


## -remarks



This structure is returned through a successful completion of an <a href="https://msdn.microsoft.com/library/windows/hardware/dn957440">IOCTL_EMI_GET_VERSION</a> IOCTL request.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn957431">Energy Metering Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn957440">IOCTL_EMI_GET_VERSION</a>
 

 

