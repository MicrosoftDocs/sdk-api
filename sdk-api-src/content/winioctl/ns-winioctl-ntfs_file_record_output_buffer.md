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

# NTFS_FILE_RECORD_OUTPUT_BUFFER structure


## -description


Receives output data from the 
<a href="https://msdn.microsoft.com/a7308fa4-0f69-4b69-bb89-5d645e2a9f6e">FSCTL_GET_NTFS_FILE_RECORD</a> control code.


## -struct-fields




### -field FileReferenceNumber

The file identifier of the returned file record. This is not necessarily the file identifier specified in the <b>FileReferenceNumber</b> member of the 
<a href="https://msdn.microsoft.com/8b0317ca-6d0e-4a04-a05a-1627d22171e3">NTFS_FILE_RECORD_INPUT_BUFFER</a> structure. Refer to the Remarks section of the reference page for 
<a href="https://msdn.microsoft.com/a7308fa4-0f69-4b69-bb89-5d645e2a9f6e">FSCTL_GET_NTFS_FILE_RECORD</a> for more information.


### -field FileRecordLength

The length of the returned file record, in bytes.


### -field FileRecordBuffer

The starting location of the buffer for the returned file record.


## -remarks



To retrieve data to fill in this structure, use the 
<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>
<a href="https://msdn.microsoft.com/a7308fa4-0f69-4b69-bb89-5d645e2a9f6e">FSCTL_GET_NTFS_FILE_RECORD</a> control code.




## -see-also




<a href="https://msdn.microsoft.com/a7308fa4-0f69-4b69-bb89-5d645e2a9f6e">FSCTL_GET_NTFS_FILE_RECORD</a>



<a href="https://msdn.microsoft.com/8b0317ca-6d0e-4a04-a05a-1627d22171e3">NTFS_FILE_RECORD_INPUT_BUFFER</a>
 

 

