---
UID: NF:comsvcs.IObjPool.PutEndTx
title: IObjPool::PutEndTx (comsvcs.h)
description: Destroys the pooled object when the transaction ends.
helpviewer_keywords: ["IObjPool interface [COM+]","PutEndTx method","IObjPool.PutEndTx","IObjPool::PutEndTx","PutEndTx","PutEndTx method [COM+]","PutEndTx method [COM+]","IObjPool interface","_cos_IObjPool_PutEndTx","comsvcs/IObjPool::PutEndTx","cos.iobjpool_putendtx"]
old-location: cos\iobjpool_putendtx.htm
tech.root: cos
ms.assetid: 24a80209-6ed8-426e-a645-463393a3a37e
ms.date: 12/05/2018
ms.keywords: IObjPool interface [COM+],PutEndTx method, IObjPool.PutEndTx, IObjPool::PutEndTx, PutEndTx, PutEndTx method [COM+], PutEndTx method [COM+],IObjPool interface, _cos_IObjPool_PutEndTx, comsvcs/IObjPool::PutEndTx, cos.iobjpool_putendtx
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IObjPool::PutEndTx
 - comsvcs/IObjPool::PutEndTx
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
 - IObjPool.PutEndTx
---

# IObjPool::PutEndTx


## -description

Destroys the pooled object when the transaction ends.

## -parameters

### -param pObj [in]

A reference to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> of the pooled object.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjpool">IObjPool</a>