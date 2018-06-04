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

# _TXFS_READ_BACKUP_INFORMATION_OUT structure


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Contains a Transactional NTFS (TxF) specific structure. This information should only be used when 
   calling 
   <a href="https://msdn.microsoft.com/777210c4-4e9b-484e-a412-8c807882facb">TXFS_WRITE_BACKUP_INFORMATION</a>.


## -struct-fields




### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.BufferLength

If the buffer is not large enough, this member receives the required buffer size.


### -field DUMMYUNIONNAME.Buffer

The buffer for the data.


## -see-also




<a href="https://msdn.microsoft.com/41c5df47-b815-47ef-bf37-d0b8030c5bfc">FSCTL_TXFS_READ_BACKUP_INFORMATION</a>
 

 

