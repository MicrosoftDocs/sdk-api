---
UID: NF:comsvcs.ITransactionProxy.CreateVoter
title: ITransactionProxy::CreateVoter method
author: windows-driver-content
description: Provides a ballot so that a COM+ transaction context can vote on the transaction.
old-location: cos\itransactionproxy_createvoter.htm
old-project: cossdk
ms.assetid: dd837082-881e-4f7e-b71e-c0f6068e3cdb
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: CreateVoter method [COM+], CreateVoter method [COM+], ITransactionProxy interface, CreateVoter,ITransactionProxy.CreateVoter, ITransactionProxy, ITransactionProxy interface [COM+], CreateVoter method, ITransactionProxy::CreateVoter, comsvcs/ITransactionProxy::CreateVoter, cos.itransactionproxy_createvoter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	ITransactionProxy.CreateVoter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ITransactionProxy::CreateVoter method


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




<a href="https://msdn.microsoft.com/58d40456-fd4f-4690-a679-3fa58b2f3cda">ITransactionProxy</a>
 

 

