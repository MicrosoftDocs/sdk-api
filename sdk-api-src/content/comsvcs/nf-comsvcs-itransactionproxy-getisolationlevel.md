---
UID: NF:comsvcs.ITransactionProxy.GetIsolationLevel
title: ITransactionProxy::GetIsolationLevel
author: windows-sdk-content
description: Retrieves the isolation level of the non-DTC transaction.
old-location: cos\itransactionproxy_getisolationlevel.htm
tech.root: cossdk
ms.assetid: a2b0e99a-0d35-4103-b7a0-407d09a2746e
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: GetIsolationLevel, GetIsolationLevel method [COM+], GetIsolationLevel method [COM+],ITransactionProxy interface, ITransactionProxy interface [COM+],GetIsolationLevel method, ITransactionProxy.GetIsolationLevel, ITransactionProxy::GetIsolationLevel, comsvcs/ITransactionProxy::GetIsolationLevel, cos.itransactionproxy_getisolationlevel
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
 - ITransactionProxy.GetIsolationLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITransactionProxy::GetIsolationLevel


## -description


Retrieves the isolation level of the non-DTC transaction.


## -parameters




### -param __MIDL__ITransactionProxy0000

TBD




#### - pIsolationLevel [out, retval]

A pointer to an <a href="http://go.microsoft.com/fwlink/p/?linkid=148531">ISOLATIONLEVEL</a> value that specifies the isolation level of the non-DTC transaction.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/58d40456-fd4f-4690-a679-3fa58b2f3cda">ITransactionProxy</a>
 

 

