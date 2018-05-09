---
UID: NF:comsvcs.IServiceTransactionConfigBase.ConfigureTransaction
title: IServiceTransactionConfigBase::ConfigureTransaction
author: windows-driver-content
description: Configures how transactions are used in the enclosed work.
old-location: cos\iservicetransactionconfigbase_configuretransaction.htm
old-project: cossdk
ms.assetid: 8277b133-2c0c-4a21-b441-457efb285178
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: ConfigureTransaction, ConfigureTransaction method [COM+], ConfigureTransaction method [COM+],IServiceTransactionConfigBase interface, IServiceTransactionConfigBase interface [COM+],ConfigureTransaction method, IServiceTransactionConfigBase.ConfigureTransaction, IServiceTransactionConfigBase::ConfigureTransaction, _cos_IServiceTransactionConfigBase_ConfigureTransaction, comsvcs/IServiceTransactionConfigBase::ConfigureTransaction, cos.iservicetransactionconfigbase_configuretransaction
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
-	IServiceTransactionConfigBase.ConfigureTransaction
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IServiceTransactionConfigBase::ConfigureTransaction


## -description


Configures how transactions are used in the enclosed work.


## -parameters




### -param transactionConfig [in]

A value from the <a href="https://msdn.microsoft.com/3524d7b3-4bcd-4e92-afc2-ddac98a23b7c">CSC_TransactionConfig</a> enumeration.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/e4740bf4-51b1-474f-9637-7c5d78f0def5">IServiceTransactionConfigBase</a>
 

 

