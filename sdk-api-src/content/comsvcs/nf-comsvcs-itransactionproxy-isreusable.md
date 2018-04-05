---
UID: NF:comsvcs.ITransactionProxy.IsReusable
title: ITransactionProxy::IsReusable method
author: windows-driver-content
description: Indicates whether the non-DTC transaction context can be reused for multiple transactions.
old-location: cos\itransactionproxy_isreusable.htm
old-project: cossdk
ms.assetid: c642d329-c996-4207-bdcf-7c79d955b2c4
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: ITransactionProxy, ITransactionProxy interface [COM+], IsReusable method, ITransactionProxy::IsReusable, IsReusable method [COM+], IsReusable method [COM+], ITransactionProxy interface, IsReusable,ITransactionProxy.IsReusable, comsvcs/ITransactionProxy::IsReusable, cos.itransactionproxy_isreusable
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
-	ITransactionProxy.IsReusable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ITransactionProxy::IsReusable method


## -description


Indicates whether the non-DTC transaction context can be reused for multiple transactions.


## -parameters




### -param pfIsReusable [out]

<b>TRUE</b> if the non-DTC transaction context can be reused for multiple transactions; otherwise, <b>FALSE</b>.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/58d40456-fd4f-4690-a679-3fa58b2f3cda">ITransactionProxy</a>
 

 

