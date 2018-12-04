---
UID: NS:emi.__unnamed_struct_1
title: EMI_METADATA_SIZE
author: windows-sdk-content
description: The EMI_METADATA_SIZE structure specifies the size of the Energy Metering Interface (EMI) metadata object that can be obtained from the device by issuing an IOCTL_EMI_GET_METADATA request.
old-location: powermeter\emi_metadata_size.htm
tech.root: powermeter
ms.assetid: EC9C71E8-7864-464B-8F16-E9D80460B36B
ms.author: windowssdkdev
ms.date: 11/06/2018
ms.keywords: EMI_METADATA_SIZE, EMI_METADATA_SIZE structure [Power Metering and Budgeting Devices], PEMI_METADATA_SIZE, PEMI_METADATA_SIZE structure pointer [Power Metering and Budgeting Devices], emi/EMI_METADATA_SIZE, emi/PEMI_METADATA_SIZE, powermeter.emi_metadata_size
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: EMI_METADATA_SIZE
req.redist: 
---

# EMI_METADATA_SIZE structure


## -description


The <b>EMI_METADATA_SIZE</b> structure specifies the size of the  Energy Metering Interface (EMI) metadata object that can be obtained from the device by issuing an <a href="https://msdn.microsoft.com/3A1A76B0-2A46-4C15-84BC-CE75701C30B7">IOCTL_EMI_GET_METADATA</a> request.


## -struct-fields




### -field MetadataSize

The size of the  EMI metadata (an <a href="https://msdn.microsoft.com/8992AA5D-7D71-4D00-9B18-FE070D29C26E">EMI_METADATA</a> structure) that can be obtained from the device.


## -remarks



This structure is returned through a successful completion of an <a href="https://msdn.microsoft.com/7A3E5BE5-F567-408A-B4AC-347E052957D9">IOCTL_EMI_GET_METADATA_SIZE</a> IOCTL request.




## -see-also




<a href="https://msdn.microsoft.com/D11C97E8-8E7F-41D7-A8A9-0B5426B20818">Energy Metering Interface</a>



<a href="https://msdn.microsoft.com/7A3E5BE5-F567-408A-B4AC-347E052957D9">IOCTL_EMI_GET_METADATA_SIZE</a>
 

 

