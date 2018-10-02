---
UID: NS:winioctl._STORAGE_HW_FIRMWARE_ACTIVATE
title: "_STORAGE_HW_FIRMWARE_ACTIVATE"
author: windows-sdk-content
description: This structure contains information about the downloaded firmware to activate.
old-location: fs\storage_hw_firmware_activate.htm
tech.root: fileio
ms.assetid: 2DAAC1FE-2503-4820-9718-9A653B0A05CA
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: "*PSTORAGE_HW_FIRMWARE_ACTIVATE, PSTORAGE_HW_FIRMWARE_ACTIVATE, PSTORAGE_HW_FIRMWARE_ACTIVATE structure pointer [Files], STORAGE_HW_FIRMWARE_ACTIVATE, STORAGE_HW_FIRMWARE_ACTIVATE structure [Files], _STORAGE_HW_FIRMWARE_ACTIVATE, fs.storage_hw_firmware_activate, winioctl/PSTORAGE_HW_FIRMWARE_ACTIVATE, winioctl/STORAGE_HW_FIRMWARE_ACTIVATE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - STORAGE_HW_FIRMWARE_ACTIVATE
product: Windows
targetos: Windows
req.typenames: STORAGE_HW_FIRMWARE_ACTIVATE, *PSTORAGE_HW_FIRMWARE_ACTIVATE
req.redist: 
---

# _STORAGE_HW_FIRMWARE_ACTIVATE structure


## -description


This structure contains information about the downloaded firmware to activate.


## -struct-fields




### -field Version

The version of this structure. This should be set to sizeof(STORAGE_HW_FIRMWARE_ACTIVATE).


### -field Size

The size of this structure. This should be set to sizeof(STORAGE_HW_FIRMWARE_ACTIVATE).


### -field Flags

The flags associated with the activation request. The following are valid flags that can be set in this member.

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>STORAGE_HW_FIRMWARE_REQUEST_FLAG_CONTROLLER</td>
<td>Indicates that the target of the request is a controller or adapter, different than the device handle or object itself (e.g. NVMe SSD or HBA).</td>
</tr>
<tr>
<td>STORAGE_HW_FIRMWARE_REQUEST_FLAG_SWITCH_TO_EXISTING_FIRMWARE</td>
<td>Indicates that the existing firmware image in the specified slot should be activated.</td>
</tr>
</table>
 


### -field Slot

The slot with the firmware image that is to be activated.


### -field Reserved0

Reserved for future use.


## -see-also




<a href="https://msdn.microsoft.com/000BEB58-D91E-4859-AC31-A4C72B84A982">IOCTL_STORAGE_FIRMWARE_ACTIVATE</a>



<a href="https://msdn.microsoft.com/77E50787-1E71-4D90-A1D3-E6665CE0EFDC">IOCTL_STORAGE_FIRMWARE_DOWNLOAD</a>



<a href="https://msdn.microsoft.com/DBF40C42-2282-4F0E-B83A-D3154D7EF332">IOCTL_STORAGE_FIRMWARE_GET_INFO</a>



<a href="https://msdn.microsoft.com/BD1D39C7-9624-400C-BF4D-5F7583AA82FB">STORAGE_HW_FIRMWARE_DOWNLOAD</a>



<a href="https://msdn.microsoft.com/7BDACD50-0FD1-4F00-BAE5-884D8C1485BC">STORAGE_HW_FIRMWARE_INFO</a>



<a href="https://msdn.microsoft.com/1A2D30F3-F2DE-40CB-BFFC-8BAD19793AE1">STORAGE_HW_FIRMWARE_INFO_QUERY</a>



<a href="https://msdn.microsoft.com/37475351-DE0F-4B80-B26B-1482FBCC16CD">STORAGE_HW_FIRMWARE_SLOT_INFO</a>
 

 

