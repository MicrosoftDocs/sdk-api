---
UID: NS:ntddpar._PAR_DEVICE_ID_SIZE_INFORMATION
title: "_PAR_DEVICE_ID_SIZE_INFORMATION"
author: windows-driver-content
description: The PAR_DEVICE_ID_SIZE_INFORMATION structure specifies the size, in bytes, of a buffer that can hold the IEEE 1284 device ID of a parallel device and a NULL terminator.
old-location: parports\par_device_id_size_information.htm
old-project: parports
ms.assetid: b48624cd-e8fb-4152-8e34-9cb1e542f62b
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PPAR_DEVICE_ID_SIZE_INFORMATION, PAR_DEVICE_ID_SIZE_INFORMATION, PAR_DEVICE_ID_SIZE_INFORMATION structure [Parallel Ports], PPAR_DEVICE_ID_SIZE_INFORMATION, PPAR_DEVICE_ID_SIZE_INFORMATION structure pointer [Parallel Ports], _PAR_DEVICE_ID_SIZE_INFORMATION, cisspd_388a088d-9dd7-4a6c-99ad-b1e725d91f72.xml, ntddpar/PAR_DEVICE_ID_SIZE_INFORMATION, ntddpar/PPAR_DEVICE_ID_SIZE_INFORMATION, parports.par_device_id_size_information"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ntddpar.h
req.include-header: Ntddpar.h
req.target-type: Windows
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
req.typenames: PAR_DEVICE_ID_SIZE_INFORMATION, *PPAR_DEVICE_ID_SIZE_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ntddpar.h
api_name:
-	PAR_DEVICE_ID_SIZE_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _PAR_DEVICE_ID_SIZE_INFORMATION structure


## -description


The PAR_DEVICE_ID_SIZE_INFORMATION structure specifies the size, in bytes, of a buffer that can hold the IEEE 1284 device ID of a parallel device and a <b>NULL</b> terminator.


## -struct-fields




### -field DeviceIdSize

Specifies the size, in bytes, of a buffer that can hold the IEEE 1284 device ID of a parallel device and a <b>NULL</b> terminator.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff544076">IOCTL_PAR_QUERY_DEVICE_ID</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544080">IOCTL_PAR_QUERY_DEVICE_ID_SIZE</a>
 

 

