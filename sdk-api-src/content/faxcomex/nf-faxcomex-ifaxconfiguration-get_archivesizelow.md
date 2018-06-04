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

# IFaxConfiguration::get_ArchiveSizeLow


## -description


The value that specifies the low-order 32-bit value (in bytes) for the size of the fax message archive.

This property is read-only.


## -parameters


## -remarks



Because the archive may exceed 4 gigabytes (GB) in size, the archive size is described using two long values. <b>ArchiveSizeLow</b> is the low 32-bit value of the archive size. <a href="https://msdn.microsoft.com/3386ec80-be4e-4105-ab57-dd634b57f67f">ArchiveSizeHigh</a> is the high 32-bit value of the archive size. The size of the archive is: <b>ArchiveSizeLow</b> + 4 GB * <b>ArchiveSizeHigh</b>. 

If both the <b>ArchiveSizeLow</b> and <a href="https://msdn.microsoft.com/3386ec80-be4e-4105-ab57-dd634b57f67f">ArchiveSizeHigh</a> properties have the value 0xffffffff, they specify an invalid archive size, and you should ignore both property values.

To read this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/20a771ed-98c3-4d26-89dc-799008954767">IFaxConfiguration</a>
 

 

