---
UID: NF:comsvcs.ITransactionProxy.CreateVoter
title: ITransactionProxy::CreateVoter (comsvcs.h)
description: Provides a ballot so that a COM+ transaction context can vote on the transaction.
helpviewer_keywords: ["CreateVoter","CreateVoter method [COM+]","CreateVoter method [COM+]","ITransactionProxy interface","ITransactionProxy interface [COM+]","CreateVoter method","ITransactionProxy.CreateVoter","ITransactionProxy::CreateVoter","comsvcs/ITransactionProxy::CreateVoter","cos.itransactionproxy_createvoter"]
old-location: cos\itransactionproxy_createvoter.htm
tech.root: cos
ms.assetid: dd837082-881e-4f7e-b71e-c0f6068e3cdb
ms.date: 12/05/2018
ms.keywords: CreateVoter, CreateVoter method [COM+], CreateVoter method [COM+],ITransactionProxy interface, ITransactionProxy interface [COM+],CreateVoter method, ITransactionProxy.CreateVoter, ITransactionProxy::CreateVoter, comsvcs/ITransactionProxy::CreateVoter, cos.itransactionproxy_createvoter
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
 - ITransactionProxy::CreateVoter
 - comsvcs/ITransactionProxy::CreateVoter
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
 - ITransactionProxy.CreateVoter
---

# ITransactionProxy::CreateVoter


## -description

Provides a ballot so that a COM+ transaction context can vote on the transaction.

## -parameters

### -param pTxAsync [in]

An implementation of <b>ITransactionVoterNotifyAsync2</b> that notifies the voter of a vote request.

### -param ppBallot [out]

An implementation of <b>ITransactionVoterBallotAsync2</b> that allows the voter to approve or veto the non-DTC transaction.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-itransactionproxy">ITransactionProxy</a>