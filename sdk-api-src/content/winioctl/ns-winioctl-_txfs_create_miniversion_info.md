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

# _TXFS_CREATE_MINIVERSION_INFO structure


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Contains the version information about the miniversion created by <a href="https://msdn.microsoft.com/3d12b149-ab34-46c4-89fc-8ddc12a81fa0">FSCTL_TXFS_CREATE_MINIVERSION</a>.


## -struct-fields




### -field StructureVersion

The version number of this <b>TXFS_CREATE_MINIVERSION_INFO</b> structure.


### -field StructureLength

The length of this <b>TXFS_CREATE_MINIVERSION_INFO</b> structure.



### -field BaseVersion

The identifier of the most recently committed version of the file.


### -field MiniVersion

The identifier of the newly-created miniversion.


## -see-also




<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/3d12b149-ab34-46c4-89fc-8ddc12a81fa0">FSCTL_TXFS_CREATE_MINIVERSION</a>
 

 

