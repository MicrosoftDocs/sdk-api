---
UID: NF:comsvcs.IObjectContext.IsInTransaction
title: IObjectContext::IsInTransaction (comsvcs.h)
description: Indicates whether the object is executing within a transaction.
helpviewer_keywords: ["IObjectContext interface [COM+]","IsInTransaction method","IObjectContext.IsInTransaction","IObjectContext::IsInTransaction","IsInTransaction","IsInTransaction method [COM+]","IsInTransaction method [COM+]","IObjectContext interface","_cos_IObjectContext_IsInTransaction","comsvcs/IObjectContext::IsInTransaction","cos.iobjectcontext_isintransaction"]
old-location: cos\iobjectcontext_isintransaction.htm
tech.root: cos
ms.assetid: 6a5582ef-0142-45df-bdad-2e3d58ca6e87
ms.date: 12/05/2018
ms.keywords: IObjectContext interface [COM+],IsInTransaction method, IObjectContext.IsInTransaction, IObjectContext::IsInTransaction, IsInTransaction, IsInTransaction method [COM+], IsInTransaction method [COM+],IObjectContext interface, _cos_IObjectContext_IsInTransaction, comsvcs/IObjectContext::IsInTransaction, cos.iobjectcontext_isintransaction
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
 - IObjectContext::IsInTransaction
 - comsvcs/IObjectContext::IsInTransaction
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
 - IObjectContext.IsInTransaction
---

# IObjectContext::IsInTransaction


## -description

Indicates whether the object is executing within a transaction.



## -returns

If the current object is executing within a transaction, the return value is <b>TRUE</b>. Otherwise, it is <b>FALSE</b>.

## -remarks

You can use this method to ensure that an object that requires a transaction never runs without one. For example, if a component that requires a transaction is improperly configured in the Component Services administration tool, you can use this method to determine that the object does not have a transaction. Then you can return an error to alert the user to the problem, or take whatever action is appropriate.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontext">IObjectContext</a>
