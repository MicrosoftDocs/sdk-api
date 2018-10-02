---
UID: NF:comsvcs.IServicePoolConfig.get_TransactionAffinity
title: IServicePoolConfig::get_TransactionAffinity
author: windows-sdk-content
description: Determines whether objects involved in transactions are held until the transaction completes.
old-location: cos\iservicepoolconfig_get_transactionaffinity.htm
tech.root: cossdk
ms.assetid: ac227f22-1ed3-4c75-8469-e8635e2d2849
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IServicePoolConfig interface [COM+],get_TransactionAffinity method, IServicePoolConfig.get_TransactionAffinity, IServicePoolConfig::get_TransactionAffinity, comsvcs/IServicePoolConfig::get_TransactionAffinity, cos.iservicepoolconfig_get_transactionaffinity, get_TransactionAffinity, get_TransactionAffinity method [COM+], get_TransactionAffinity method [COM+],IServicePoolConfig interface
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
 - IServicePoolConfig.get_TransactionAffinity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IServicePoolConfig::get_TransactionAffinity


## -description


Determines whether objects involved in transactions are held until the transaction completes.


## -parameters




### -param pfTxAffinity [in]

<b>TRUE</b> if the objects are held and <b>FALSE</b> otherwise.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/026abfcf-56b5-4821-a9d4-37beeb3a052b">IServicePoolConfig</a>
 

 

