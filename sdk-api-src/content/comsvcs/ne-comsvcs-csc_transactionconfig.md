---
UID: NE:comsvcs.tagCSC_TransactionConfig
title: CSC_TransactionConfig (comsvcs.h)
author: windows-sdk-content
description: Indicates how transactions are configured for CServiceConfig.
old-location: cos\csc_transactionconfig.htm
tech.root: cossdk
ms.assetid: 3524d7b3-4bcd-4e92-afc2-ddac98a23b7c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CSC_CreateTransactionIfNecessary, CSC_IfContainerIsTransactional, CSC_NewTransaction, CSC_NoTransaction, CSC_TransactionConfig, CSC_TransactionConfig enumeration [COM+], _cos_CSC_TransactionConfig, comsvcs/CSC_CreateTransactionIfNecessary, comsvcs/CSC_IfContainerIsTransactional, comsvcs/CSC_NewTransaction, comsvcs/CSC_NoTransaction, comsvcs/CSC_TransactionConfig, cos.csc_transactionconfig
ms.topic: enum
f1_keywords: 
 - "comsvcs/CSC_TransactionConfig"
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - HeaderDef
api_location:
 - ComSvcs.h
api_name:
 - CSC_TransactionConfig
product: Windows
targetos: Windows
req.typenames: CSC_TransactionConfig
req.redist: 
ms.custom: 19H1
---

# CSC_TransactionConfig enumeration


## -description


Indicates how transactions are configured for <a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>.


## -enum-fields




### -field CSC_NoTransaction

Transactions are never used within the enclosed context. This is the default transaction setting for <a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> when <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/ne-comsvcs-csc_inheritanceconfig">CSC_InheritanceConfig</a> is set to CSC_Ignore.


### -field CSC_IfContainerIsTransactional

Transactions are used only if the enclosed context is using a transaction; a new transaction is never created. This is the default transaction setting for <a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> when <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/ne-comsvcs-csc_inheritanceconfig">CSC_InheritanceConfig</a> is set to CSC_Inherit.


### -field CSC_CreateTransactionIfNecessary

Transactions are always used. The existing transaction is used, or if the enclosed context does not already use transactions, a new transaction is created.


### -field CSC_NewTransaction

A new transaction is always created.



## -remarks



This enumeration is used to configure transactions through <a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> for either the work submitted through the activity created by <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a> or the work that is enclosed between calls to <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a> and <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-coleaveservicedomain">CoLeaveServiceDomain</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--transactions">COM+ Transactions</a>



<a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicetransactionconfigbase-configuretransaction">IServiceTransactionConfigBase::ConfigureTransaction</a>
 

 

