---
UID: NF:comsvcs.IMessageMover.MoveMessages
title: IMessageMover::MoveMessages (comsvcs.h)
description: Moves all messages from the source queue to the destination queue.
helpviewer_keywords: ["IMessageMover interface [COM+]","MoveMessages method","IMessageMover.MoveMessages","IMessageMover::MoveMessages","MoveMessages","MoveMessages method [COM+]","MoveMessages method [COM+]","IMessageMover interface","_cos_IMessageMover_MoveMessages","comsvcs/IMessageMover::MoveMessages","cos.imessagemover_movemessages"]
old-location: cos\imessagemover_movemessages.htm
tech.root: cos
ms.assetid: ebe06730-710b-42ce-b905-be87971b19c3
ms.date: 12/05/2018
ms.keywords: IMessageMover interface [COM+],MoveMessages method, IMessageMover.MoveMessages, IMessageMover::MoveMessages, MoveMessages, MoveMessages method [COM+], MoveMessages method [COM+],IMessageMover interface, _cos_IMessageMover_MoveMessages, comsvcs/IMessageMover::MoveMessages, cos.imessagemover_movemessages
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMessageMover::MoveMessages
 - comsvcs/IMessageMover::MoveMessages
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IMessageMover.MoveMessages
---

# IMessageMover::MoveMessages


## -description

Moves all messages from the source queue to the destination queue.

## -parameters

### -param plMessagesMoved [out]

The number of messages that were moved from the source to the destination queue.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Messages are moved one at a time unless both the source and destination queue are transacted. In this case, <a href="/windows/desktop/api/comsvcs/nf-comsvcs-imessagemover-get_commitbatchsize">CommitBatchSize</a> specifies the number of messages that are moved before <a href="/windows/desktop/api/comsvcs/nf-comsvcs-itransactioncontext-commit">Commit</a> is invoked. There is no provision for moving fewer than all of the messages on the queue.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imessagemover">IMessageMover</a>