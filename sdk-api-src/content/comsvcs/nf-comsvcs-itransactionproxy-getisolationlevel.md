---
UID: NF:comsvcs.ITransactionProxy.GetIsolationLevel
title: ITransactionProxy::GetIsolationLevel (comsvcs.h)
description: Retrieves the isolation level of the non-DTC transaction.
helpviewer_keywords: ["GetIsolationLevel","GetIsolationLevel method [COM+]","GetIsolationLevel method [COM+]","ITransactionProxy interface","ITransactionProxy interface [COM+]","GetIsolationLevel method","ITransactionProxy.GetIsolationLevel","ITransactionProxy::GetIsolationLevel","comsvcs/ITransactionProxy::GetIsolationLevel","cos.itransactionproxy_getisolationlevel"]
old-location: cos\itransactionproxy_getisolationlevel.htm
tech.root: cos
ms.assetid: a2b0e99a-0d35-4103-b7a0-407d09a2746e
ms.date: 12/05/2018
ms.keywords: GetIsolationLevel, GetIsolationLevel method [COM+], GetIsolationLevel method [COM+],ITransactionProxy interface, ITransactionProxy interface [COM+],GetIsolationLevel method, ITransactionProxy.GetIsolationLevel, ITransactionProxy::GetIsolationLevel, comsvcs/ITransactionProxy::GetIsolationLevel, cos.itransactionproxy_getisolationlevel
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
 - ITransactionProxy::GetIsolationLevel
 - comsvcs/ITransactionProxy::GetIsolationLevel
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
 - ITransactionProxy.GetIsolationLevel
---

# ITransactionProxy::GetIsolationLevel


## -description

Retrieves the isolation level of the non-DTC transaction.

## -parameters

### -param __MIDL__ITransactionProxy0000 [out, retval]

A pointer to an <a href="/previous-versions/windows/desktop/ms679234(v=vs.85)">ISOLATIONLEVEL</a> value that specifies the isolation level of the non-DTC transaction.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-itransactionproxy">ITransactionProxy</a>