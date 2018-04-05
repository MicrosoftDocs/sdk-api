---
UID: NS:winioctl._STORAGE_HW_FIRMWARE_INFO_QUERY
title: "_STORAGE_HW_FIRMWARE_INFO_QUERY"
author: windows-driver-content
description: This structure contains information about the device firmware.
old-location: fs\storage_hw_firmware_info_query.htm
old-project: FileIO
ms.assetid: 1A2D30F3-F2DE-40CB-BFFC-8BAD19793AE1
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: "*PSTORAGE_HW_FIRMWARE_INFO_QUERY, PSTORAGE_HW_FIRMWARE_INFO_QUERY, PSTORAGE_HW_FIRMWARE_INFO_QUERY structure pointer [Files], STORAGE_HW_FIRMWARE_INFO_QUERY, STORAGE_HW_FIRMWARE_INFO_QUERY structure [Files], _STORAGE_HW_FIRMWARE_INFO_QUERY, fs.storage_hw_firmware_info_query, winioctl/PSTORAGE_HW_FIRMWARE_INFO_QUERY, winioctl/STORAGE_HW_FIRMWARE_INFO_QUERY"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: STORAGE_HW_FIRMWARE_INFO_QUERY, *PSTORAGE_HW_FIRMWARE_INFO_QUERY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winioctl.h.h
api_name:
-	STORAGE_HW_FIRMWARE_INFO_QUERY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _STORAGE_HW_FIRMWARE_INFO_QUERY structure


## -description


This structure contains information about the device firmware.


## -struct-fields




### -field Version

The version of this structure. This should be set to sizeof(STORAGE_HW_FIRMWARE_INFO_QUERY)


### -field Size

The size of this structure as a buffer.


### -field Flags

The flags associated with the query. The following are flags that can be set in this member.

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>STORAGE_HW_FIRMWARE_REQUEST_FLAG_CONTROLLER</td>
<td>Indicates that the target of the request other than the device hand/object itself.</td>
</tr>
</table>
 


### -field Reserved

Reserved for future use.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn932065">IOCTL_STORAGE_FIRMWARE_ACTIVATE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn932066">IOCTL_STORAGE_FIRMWARE_DOWNLOAD</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn932067">IOCTL_STORAGE_FIRMWARE_GET_INFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn931808">STORAGE_HW_FIRMWARE_ACTIVATE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn931809">STORAGE_HW_FIRMWARE_DOWNLOAD</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn931810">STORAGE_HW_FIRMWARE_INFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn931812">STORAGE_HW_FIRMWARE_SLOT_INFO</a>
 

 

