---
UID: NF:comsvcs.IServiceSysTxnConfig.ConfigureBYOTSysTxn
title: IServiceSysTxnConfig::ConfigureBYOTSysTxn method
author: windows-driver-content
description: Enables you to run the enclosed code in the scope of an existing transaction that you specify with a transaction proxy.
old-location: cos\iservicesystxnconfig_configurebyotsystxn.htm
old-project: cossdk
ms.assetid: 6023e756-7797-489b-96fd-9cf2d9f2cb2b
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: ConfigureBYOTSysTxn method [COM+], ConfigureBYOTSysTxn method [COM+], IServiceSysTxnConfig interface, ConfigureBYOTSysTxn,IServiceSysTxnConfig.ConfigureBYOTSysTxn, IServiceSysTxnConfig, IServiceSysTxnConfig interface [COM+], ConfigureBYOTSysTxn method, IServiceSysTxnConfig::ConfigureBYOTSysTxn, comsvcs/IServiceSysTxnConfig::ConfigureBYOTSysTxn, cos.iservicesystxnconfig_configurebyotsystxn
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
-	IServiceSysTxnConfig.ConfigureBYOTSysTxn
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IServiceSysTxnConfig::ConfigureBYOTSysTxn method


## -description


Enables you to run the enclosed code in the scope of an existing transaction that you specify with a transaction proxy.


## -parameters




### -param pTxProxy [in]

The <a href="https://msdn.microsoft.com/58d40456-fd4f-4690-a679-3fa58b2f3cda">ITransactionProxy</a> interface of the existing transaction in which you will run the enclosed code.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/8e721496-fc2b-46b8-ae28-432da6c429e6">IServiceSysTxnConfig</a>
 

 

