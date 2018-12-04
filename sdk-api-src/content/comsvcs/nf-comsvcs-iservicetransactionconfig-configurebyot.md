---
UID: NF:comsvcs.IServiceTransactionConfig.ConfigureBYOT
title: IServiceTransactionConfig::ConfigureBYOT
author: windows-sdk-content
description: Enables you to configure the transaction that you use when you bring your own transaction.
old-location: cos\iservicetransactionconfig_configurebyot.htm
tech.root: cossdk
ms.assetid: be4fa727-962e-4254-8615-58f6ced15fc3
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ConfigureBYOT, ConfigureBYOT method [COM+], ConfigureBYOT method [COM+],IServiceTransactionConfig interface, IServiceTransactionConfig interface [COM+],ConfigureBYOT method, IServiceTransactionConfig.ConfigureBYOT, IServiceTransactionConfig::ConfigureBYOT, _cos_IServiceTransactionConfig_ConfigureBYOT, comsvcs/IServiceTransactionConfig::ConfigureBYOT, cos.iservicetransactionconfig_configurebyot
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
 - IServiceTransactionConfig.ConfigureBYOT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IServiceTransactionConfig::ConfigureBYOT


## -description


Enables you to configure the transaction that you use when you bring your own transaction.


## -parameters




### -param pITxByot [in]

A pointer to the <b>ITransaction</b> interface of the existing transaction in which you want to run the enclosed code.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -remarks



When you bring your own transaction, that transaction's settings override the settings from the inherited methods of the <a href="https://msdn.microsoft.com/7f31c590-8290-4556-9fcf-e27db01bad93">IServiceTransactionConfig</a> interface.

The <b>ConfigureBYOT</b> and the <a href="https://msdn.microsoft.com/fcd65d90-8855-41e9-a22d-d2b1d46e98fa">IServiceTransactionConfigBase::BringYourOwnTransaction</a> methods are identical in behavior; the only difference is the type of parameter passed to each method.




## -see-also




<a href="https://msdn.microsoft.com/492875cb-52a7-484f-810e-bd838373b603">Bring Your Own Transaction (BYOT)</a>



<a href="https://msdn.microsoft.com/7f31c590-8290-4556-9fcf-e27db01bad93">IServiceTransactionConfig</a>
 

 

