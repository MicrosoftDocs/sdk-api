---
UID: NF:comsvcs.IServiceTransactionConfigBase.IsolationLevel
title: IServiceTransactionConfigBase::IsolationLevel (comsvcs.h)
description: Sets the isolation level of the transactions.
helpviewer_keywords: ["IServiceTransactionConfigBase interface [COM+]","IsolationLevel method","IServiceTransactionConfigBase.IsolationLevel","IServiceTransactionConfigBase::IsolationLevel","IsolationLevel","IsolationLevel method [COM+]","IsolationLevel method [COM+]","IServiceTransactionConfigBase interface","_cos_IServiceTransactionConfigBase_IsolationLevel","comsvcs/IServiceTransactionConfigBase::IsolationLevel","cos.iservicetransactionconfigbase_isolationlevel"]
old-location: cos\iservicetransactionconfigbase_isolationlevel.htm
tech.root: cos
ms.assetid: 4595239b-30e7-4b03-a2c7-7061cbf28bac
ms.date: 12/05/2018
ms.keywords: IServiceTransactionConfigBase interface [COM+],IsolationLevel method, IServiceTransactionConfigBase.IsolationLevel, IServiceTransactionConfigBase::IsolationLevel, IsolationLevel, IsolationLevel method [COM+], IsolationLevel method [COM+],IServiceTransactionConfigBase interface, _cos_IServiceTransactionConfigBase_IsolationLevel, comsvcs/IServiceTransactionConfigBase::IsolationLevel, cos.iservicetransactionconfigbase_isolationlevel
f1_keywords:
- comsvcs/IServiceTransactionConfigBase.IsolationLevel
dev_langs:
- c++
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
- IServiceTransactionConfigBase.IsolationLevel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IServiceTransactionConfigBase::IsolationLevel


## -description


Sets the isolation level of the transactions.



## -parameters




### -param option [in]

A value from the <a href="https://docs.microsoft.com/windows/desktop/api/comadmin/ne-comadmin-comadmintxisolationleveloptions">COMAdminTxIsolationLevelOptions</a> enumeration.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -remarks



A new transaction is created if the enclosing transaction is not running at the specified isolation level. This method is ignored if the enclosed code would not otherwise run in a transaction.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iservicetransactionconfigbase">IServiceTransactionConfigBase</a>
 

 

