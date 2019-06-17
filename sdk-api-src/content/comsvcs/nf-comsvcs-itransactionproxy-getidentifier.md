---
UID: NF:comsvcs.ITransactionProxy.GetIdentifier
title: ITransactionProxy::GetIdentifier (comsvcs.h)
author: windows-sdk-content
description: Retrieves the identifier of the non-DTC transaction.
old-location: cos\itransactionproxy_getidentifier.htm
tech.root: cossdk
ms.assetid: 8045989b-7b66-4340-a06e-4b4102d09784
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetIdentifier, GetIdentifier method [COM+], GetIdentifier method [COM+],ITransactionProxy interface, ITransactionProxy interface [COM+],GetIdentifier method, ITransactionProxy.GetIdentifier, ITransactionProxy::GetIdentifier, comsvcs/ITransactionProxy::GetIdentifier, cos.itransactionproxy_getidentifier
ms.topic: method
f1_keywords: ["comsvcs/ITransactionProxy.GetIdentifier"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ITransactionProxy.GetIdentifier
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITransactionProxy::GetIdentifier


## -description


Retrieves the identifier of the non-DTC transaction.


## -parameters




### -param pbstrIdentifier [out, retval]

The GUID that identifies the non-DTC transaction.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-itransactionproxy">ITransactionProxy</a>
 

 

