---
UID: NF:comsvcs.IMessageMover.put_CommitBatchSize
title: IMessageMover::put_CommitBatchSize (comsvcs.h)
author: windows-sdk-content
description: Sets the commit batch size. This is the number of messages that should be moved from source to destination queue between commit operations.
old-location: cos\imessagemover_put_commitbatchsize.htm
tech.root: cossdk
ms.assetid: 107a934b-565e-444d-a042-2325b8f18754
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMessageMover interface [COM+],put_CommitBatchSize method, IMessageMover.put_CommitBatchSize, IMessageMover::put_CommitBatchSize, comsvcs/IMessageMover::put_CommitBatchSize, cos.imessagemover_put_commitbatchsize, put_CommitBatchSize, put_CommitBatchSize method [COM+], put_CommitBatchSize method [COM+],IMessageMover interface
ms.topic: method
f1_keywords: 
 - "comsvcs/IMessageMover.put_CommitBatchSize"
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
 - IMessageMover.put_CommitBatchSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-imessagemover">IMessageMover</a>
 

 

