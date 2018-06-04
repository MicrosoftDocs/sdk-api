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

# EMI_METADATA_SIZE structure


## -description


The <b>EMI_METADATA_SIZE</b> structure specifies the size of the  Energy Metering Interface (EMI) metadata object that can be obtained from the device by issuing an <a href="https://msdn.microsoft.com/library/windows/hardware/dn957436">IOCTL_EMI_GET_METADATA</a> request.


## -struct-fields




### -field MetadataSize

The size of the  EMI metadata (an <a href="https://msdn.microsoft.com/library/windows/hardware/dn957428">EMI_METADATA</a> structure) that can be obtained from the device.


## -remarks



This structure is returned through a successful completion of an <a href="https://msdn.microsoft.com/library/windows/hardware/dn957438">IOCTL_EMI_GET_METADATA_SIZE</a> IOCTL request.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn957431">Energy Metering Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn957438">IOCTL_EMI_GET_METADATA_SIZE</a>
 

 

