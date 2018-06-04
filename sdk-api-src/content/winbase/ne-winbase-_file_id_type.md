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

# _FILE_ID_TYPE enumeration


## -description


Discriminator for the union in the 
    <a href="https://msdn.microsoft.com/9092a701-3b47-4c4c-8221-54fa3220d322">FILE_ID_DESCRIPTOR</a> structure.


## -enum-fields




### -field FileIdType

Use the <b>FileId</b> member of the union.


### -field ObjectIdType

Use the <b>ObjectId</b> member of the union.


### -field ExtendedFileIdType

Use the <b>ExtendedFileId</b> member of the union.
      

<b>Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008, Windows 7 and Windows Server 2008 R2:  </b>This value is not supported before Windows 8 and Windows Server 2012.


### -field MaximumFileIdType

This value is used for comparison only. All valid values are less than this value.


## -see-also




<a href="https://msdn.microsoft.com/9092a701-3b47-4c4c-8221-54fa3220d322">FILE_ID_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/14b1cfff-5e47-4309-8e62-fb5c8da9ce97">File Management Enumerations</a>



<a href="https://msdn.microsoft.com/caa757a2-fc3f-4883-8d3e-b98d28f92517">OpenFileById</a>
 

 

