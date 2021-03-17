---
UID: NF:comsvcs.ITransactionProxy.IsReusable
title: ITransactionProxy::IsReusable (comsvcs.h)
description: Indicates whether the non-DTC transaction context can be reused for multiple transactions.
helpviewer_keywords: ["ITransactionProxy interface [COM+]","IsReusable method","ITransactionProxy.IsReusable","ITransactionProxy::IsReusable","IsReusable","IsReusable method [COM+]","IsReusable method [COM+]","ITransactionProxy interface","comsvcs/ITransactionProxy::IsReusable","cos.itransactionproxy_isreusable"]
old-location: cos\itransactionproxy_isreusable.htm
tech.root: cos
ms.assetid: c642d329-c996-4207-bdcf-7c79d955b2c4
ms.date: 12/05/2018
ms.keywords: ITransactionProxy interface [COM+],IsReusable method, ITransactionProxy.IsReusable, ITransactionProxy::IsReusable, IsReusable, IsReusable method [COM+], IsReusable method [COM+],ITransactionProxy interface, comsvcs/ITransactionProxy::IsReusable, cos.itransactionproxy_isreusable
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
 - ITransactionProxy::IsReusable
 - comsvcs/ITransactionProxy::IsReusable
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
 - ITransactionProxy.IsReusable
---

# ITransactionProxy::IsReusable


## -description

Indicates whether the non-DTC transaction context can be reused for multiple transactions.

## -parameters

### -param pfIsReusable [out]

<b>TRUE</b> if the non-DTC transaction context can be reused for multiple transactions; otherwise, <b>FALSE</b>.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-itransactionproxy">ITransactionProxy</a>