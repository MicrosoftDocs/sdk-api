---
UID: NF:comsvcs.IServiceTransactionConfigBase.IsolationLevel
title: IServiceTransactionConfigBase::IsolationLevel
author: windows-sdk-content
description: Sets the isolation level of the transactions.
old-location: cos\iservicetransactionconfigbase_isolationlevel.htm
old-project: cossdk
ms.assetid: 4595239b-30e7-4b03-a2c7-7061cbf28bac
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IServiceTransactionConfigBase interface [COM+],IsolationLevel method, IServiceTransactionConfigBase.IsolationLevel, IServiceTransactionConfigBase::IsolationLevel, IsolationLevel, IsolationLevel method [COM+], IsolationLevel method [COM+],IServiceTransactionConfigBase interface, _cos_IServiceTransactionConfigBase_IsolationLevel, comsvcs/IServiceTransactionConfigBase::IsolationLevel, cos.iservicetransactionconfigbase_isolationlevel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IServiceTransactionConfigBase.IsolationLevel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IServiceTransactionConfigBase::IsolationLevel


## -description


Sets the isolation level of the transactions.



## -parameters




### -param option [in]

A value from the <a href="https://msdn.microsoft.com/5e407423-b116-48c5-a99c-2551eca379b3">COMAdminTxIsolationLevelOptions</a> enumeration.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -remarks



A new transaction is created if the enclosing transaction is not running at the specified isolation level. This method is ignored if the enclosed code would not otherwise run in a transaction.





## -see-also




<a href="https://msdn.microsoft.com/e4740bf4-51b1-474f-9637-7c5d78f0def5">IServiceTransactionConfigBase</a>
 

 

