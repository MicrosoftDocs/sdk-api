---
UID: NF:comsvcs.IServicePoolConfig.put_TransactionAffinity
title: IServicePoolConfig::put_TransactionAffinity method
author: windows-driver-content
description: Sets whether objects involved in transactions are held until the transaction completes.
old-location: cos\iservicepoolconfig_put_transactionaffinity.htm
old-project: cossdk
ms.assetid: 2f69bae2-560d-455b-b1b4-922c2fb4563a
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: IServicePoolConfig, IServicePoolConfig interface [COM+], put_TransactionAffinity method, IServicePoolConfig::put_TransactionAffinity, comsvcs/IServicePoolConfig::put_TransactionAffinity, cos.iservicepoolconfig_put_transactionaffinity, put_TransactionAffinity method [COM+], put_TransactionAffinity method [COM+], IServicePoolConfig interface, put_TransactionAffinity,IServicePoolConfig.put_TransactionAffinity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IServicePoolConfig.put_TransactionAffinity
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IServicePoolConfig::put_TransactionAffinity method


## -description


Sets whether objects involved in transactions are held until the transaction completes.


## -parameters




### -param fTxAffinity [in]

<b>TRUE</b> if the objects are to be held and <b>FALSE</b> otherwise.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/026abfcf-56b5-4821-a9d4-37beeb3a052b">IServicePoolConfig</a>
 

 

