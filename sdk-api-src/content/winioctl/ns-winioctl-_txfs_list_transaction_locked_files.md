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

# _TXFS_LIST_TRANSACTION_LOCKED_FILES structure


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Contains a list of files locked by a transacted writer.


## -struct-fields




### -field KtmTransaction

The KTM transaction to enumerate locked files for in this RM.


### -field NumberOfFiles

The number of files involved for the specified transaction on this resource manager.


### -field BufferSizeRequired

The length of the buffer required to hold the complete list of files at the time of this call. This is not guaranteed to be the same length as any other subsequent call.


### -field Offset

The offset from the beginning of this structure to the beginning of the first <a href="https://msdn.microsoft.com/220ccb27-c7a2-4d4e-8efd-5c8f8d1697cd">TXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/fdef45fd-b197-4428-96c5-ac91b43681b1">FSCTL_TXFS_LIST_TRANSACTION_LOCKED_FILES</a>



<a href="https://msdn.microsoft.com/220ccb27-c7a2-4d4e-8efd-5c8f8d1697cd">TXFS_LIST_TRANSACTION_LOCKED_FILES_ENTRY</a>
 

 

