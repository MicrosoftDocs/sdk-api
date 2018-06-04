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

# NTFS_FILE_RECORD_INPUT_BUFFER structure


## -description


Contains data for the 
<a href="https://msdn.microsoft.com/a7308fa4-0f69-4b69-bb89-5d645e2a9f6e">FSCTL_GET_NTFS_FILE_RECORD</a> control code.


## -struct-fields




### -field FileReferenceNumber

The file identifier of the file record to be retrieved. This is not necessarily the file identifier returned in the <b>FileReferenceNumber</b> member of the 
<a href="https://msdn.microsoft.com/e2597939-5159-4c35-9a1f-f3be43081d72">NTFS_FILE_RECORD_OUTPUT_BUFFER</a> structure. Refer to the Remarks section of the reference page for 
<a href="https://msdn.microsoft.com/a7308fa4-0f69-4b69-bb89-5d645e2a9f6e">FSCTL_GET_NTFS_FILE_RECORD</a> for more information.
					


## -remarks



Pass this structure as input to the 
<a href="https://msdn.microsoft.com/a7308fa4-0f69-4b69-bb89-5d645e2a9f6e">FSCTL_GET_NTFS_FILE_RECORD</a> control code.




## -see-also




<a href="https://msdn.microsoft.com/a7308fa4-0f69-4b69-bb89-5d645e2a9f6e">FSCTL_GET_NTFS_FILE_RECORD</a>



<a href="https://msdn.microsoft.com/e2597939-5159-4c35-9a1f-f3be43081d72">NTFS_FILE_RECORD_OUTPUT_BUFFER</a>
 

 

