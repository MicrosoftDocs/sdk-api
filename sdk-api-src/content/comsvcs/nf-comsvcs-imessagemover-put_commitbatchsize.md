---
UID: NF:comsvcs.IMessageMover.put_CommitBatchSize
title: IMessageMover::put_CommitBatchSize
author: windows-driver-content
description: Sets the commit batch size. This is the number of messages that should be moved from source to destination queue between commit operations.
old-location: cos\imessagemover_put_commitbatchsize.htm
old-project: cossdk
ms.assetid: 107a934b-565e-444d-a042-2325b8f18754
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: IMessageMover interface [COM+],put_CommitBatchSize method, IMessageMover.put_CommitBatchSize, IMessageMover::put_CommitBatchSize, comsvcs/IMessageMover::put_CommitBatchSize, cos.imessagemover_put_commitbatchsize, put_CommitBatchSize, put_CommitBatchSize method [COM+], put_CommitBatchSize method [COM+],IMessageMover interface
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IMessageMover.put_CommitBatchSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IMessageMover::put_CommitBatchSize


## -description


Sets the commit batch size. This is the number of messages that should be moved from source to destination queue between commit operations.


## -parameters




### -param newVal [in]

The commit batch size.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/aa7c57a2-0dee-4f18-bce4-4fcc47d4d7a7">IMessageMover</a>
 

 

