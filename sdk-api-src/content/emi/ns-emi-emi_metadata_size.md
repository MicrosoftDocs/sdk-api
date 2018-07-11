---
UID: NS:emi.EMI_METADATA_SIZE
title: EMI_METADATA_SIZE
author: windows-sdk-content
description: The EMI_METADATA_SIZE structure specifies the size of the Energy Metering Interface (EMI) metadata object that can be obtained from the device by issuing an IOCTL_EMI_GET_METADATA request.
old-location: powermeter\emi_metadata_size.htm
old-project: powermeter
ms.assetid: EC9C71E8-7864-464B-8F16-E9D80460B36B
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: EMI_METADATA_SIZE, EMI_METADATA_SIZE structure [Power Metering and Budgeting Devices], PEMI_METADATA_SIZE, PEMI_METADATA_SIZE structure pointer [Power Metering and Budgeting Devices], emi/EMI_METADATA_SIZE, emi/PEMI_METADATA_SIZE, powermeter.emi_metadata_size
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: emi.h
req.include-header: Emi.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows 10.
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
tech.root: 
req.typenames: EMI_METADATA_SIZE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - emi.h
api_name:
 - EMI_METADATA_SIZE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 

