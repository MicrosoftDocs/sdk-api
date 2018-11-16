---
UID: NF:comsvcs.IMessageMover.MoveMessages
title: IMessageMover::MoveMessages
author: windows-sdk-content
description: Moves all messages from the source queue to the destination queue.
old-location: cos\imessagemover_movemessages.htm
tech.root: cossdk
ms.assetid: ebe06730-710b-42ce-b905-be87971b19c3
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMessageMover interface [COM+],MoveMessages method, IMessageMover.MoveMessages, IMessageMover::MoveMessages, MoveMessages, MoveMessages method [COM+], MoveMessages method [COM+],IMessageMover interface, _cos_IMessageMover_MoveMessages, comsvcs/IMessageMover::MoveMessages, cos.imessagemover_movemessages
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IMessageMover.MoveMessages
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- comsvcs.h
: 
- IMessageMover.MoveMessages
: 
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



Messages are moved one at a time unless both the source and destination queue are transacted. In this case, <a href="https://msdn.microsoft.com/7c0b5ebb-00dc-4c9a-9c0c-6d92cd13f534">CommitBatchSize</a> specifies the number of messages that are moved before <a href="https://msdn.microsoft.com/3945fdf1-6361-413e-9621-18871ded47a4">Commit</a> is invoked. There is no provision for moving fewer than all of the messages on the queue.





## -see-also




<a href="https://msdn.microsoft.com/aa7c57a2-0dee-4f18-bce4-4fcc47d4d7a7">IMessageMover</a>
 

 

