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

# IMessageMover::MoveMessages


## -description


Moves all messages from the source queue to the destination queue.


## -parameters




### -param plMessagesMoved [out]

The number of messages that were moved from the source to the destination queue.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Messages are moved one at a time unless both the source and destination queue are transacted. In this case, <a href="https://msdn.microsoft.com/7c0b5ebb-00dc-4c9a-9c0c-6d92cd13f534">CommitBatchSize</a> specifies the number of messages that are moved before <a href="https://msdn.microsoft.com/library/windows/hardware/hh439717">Commit</a> is invoked. There is no provision for moving fewer than all of the messages on the queue.





## -see-also




<a href="https://msdn.microsoft.com/aa7c57a2-0dee-4f18-bce4-4fcc47d4d7a7">IMessageMover</a>
 

 

