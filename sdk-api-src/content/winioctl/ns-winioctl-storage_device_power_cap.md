---
UID: NS:winioctl._STORAGE_DEVICE_POWER_CAP
title: STORAGE_DEVICE_POWER_CAP
author: windows-sdk-content
description: This structure is used as an input and output buffer for the IOCTL_STORAGE_DEVICE_POWER_CAP.
old-location: fs\storage_device_power_cap.htm
tech.root: fileio
ms.assetid: B81C7D08-980E-4BA2-8CF8-7B6E58709102
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PSTORAGE_DEVICE_POWER_CAP, PSTORAGE_DEVICE_POWER_CAP, PSTORAGE_DEVICE_POWER_CAP structure pointer [Files], STORAGE_DEVICE_POWER_CAP, STORAGE_DEVICE_POWER_CAP structure [Files], fs.storage_device_power_cap, winioctl/PSTORAGE_DEVICE_POWER_CAP, winioctl/STORAGE_DEVICE_POWER_CAP"
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
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
 - winioctl.h
api_name:
 - STORAGE_DEVICE_POWER_CAP
product: Windows
targetos: Windows
req.typenames: STORAGE_DEVICE_POWER_CAP, *PSTORAGE_DEVICE_POWER_CAP
req.redist: 
---

# STORAGE_DEVICE_POWER_CAP structure


## -description


This structure is used as an input and output buffer for the <a href="https://msdn.microsoft.com/4BF06CA7-5219-4EE0-9A74-F43035914332">IOCTL_STORAGE_DEVICE_POWER_CAP</a>.


## -struct-fields




### -field Version

The version of this structure. This should be set to STORAGE_DEVICE_POWER_CAP_VERSION_V1.


### -field Size

The size of this structure.


### -field Units

The units of the <i>MaxPower</i> value, of type <a href="https://msdn.microsoft.com/A6C48765-9A18-4F77-8B0F-9653CE6FDE23">STORAGE_DEVICE_POWER_CAP_UNITS</a>.


### -field MaxPower

Contains the value of the actual maximum power consumption level of the device. This may be equal to, less than, or greater than the desired threshold, depending on what the device supports.

