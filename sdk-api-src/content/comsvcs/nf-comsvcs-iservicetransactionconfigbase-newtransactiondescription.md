---
UID: NF:comsvcs.IServiceTransactionConfigBase.NewTransactionDescription
title: IServiceTransactionConfigBase::NewTransactionDescription
author: windows-sdk-content
description: Sets the name that is used when transaction statistics are displayed.
old-location: cos\iservicetransactionconfigbase_newtransactiondescription.htm
old-project: cossdk
ms.assetid: ecdc160b-168d-48f4-bbe3-46d654ee8607
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IServiceTransactionConfigBase interface [COM+],NewTransactionDescription method, IServiceTransactionConfigBase.NewTransactionDescription, IServiceTransactionConfigBase::NewTransactionDescription, NewTransactionDescription, NewTransactionDescription method [COM+], NewTransactionDescription method [COM+],IServiceTransactionConfigBase interface, _cos_IServiceTransactionConfigBase_NewTransactionDescription, comsvcs/IServiceTransactionConfigBase::NewTransactionDescription, cos.iservicetransactionconfigbase_newtransactiondescription
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
 - IServiceTransactionConfigBase.NewTransactionDescription
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IServiceTransactionConfigBase::NewTransactionDescription


## -description


Sets the name that is used when transaction statistics are displayed.



## -parameters




### -param szTxDesc [in]

The description of the transaction.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_FAIL, and S_OK.




## -remarks



If you do not provide a description by using this method, the value of the <i>szTrackerCtxName</i> parameter from the <a href="https://msdn.microsoft.com/cdeb982b-720a-4d69-9c3c-d7a5a4527991">IServiceTrackerConfig::TrackerConfig</a> method is used to describe the transaction.




## -see-also




<a href="https://msdn.microsoft.com/e4740bf4-51b1-474f-9637-7c5d78f0def5">IServiceTransactionConfigBase</a>
 

 

