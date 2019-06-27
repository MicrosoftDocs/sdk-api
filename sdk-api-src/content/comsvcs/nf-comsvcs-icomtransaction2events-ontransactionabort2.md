---
UID: NF:comsvcs.IComTransaction2Events.OnTransactionAbort2
title: IComTransaction2Events::OnTransactionAbort2 (comsvcs.h)
author: windows-sdk-content
description: Generated when a transaction aborts.
old-location: cos\icomtransaction2events_ontransactionabort2.htm
tech.root: cossdk
ms.assetid: 8c74410c-c9a0-4115-876b-4b4db798e54f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IComTransaction2Events interface [COM+],OnTransactionAbort2 method, IComTransaction2Events.OnTransactionAbort2, IComTransaction2Events::OnTransactionAbort2, OnTransactionAbort2, OnTransactionAbort2 method [COM+], OnTransactionAbort2 method [COM+],IComTransaction2Events interface, _dtc_icomtransaction2events_ontransactionabort2, comsvcs/IComTransaction2Events::OnTransactionAbort2, cos.icomtransaction2events_ontransactionabort2
ms.topic: method
f1_keywords: 
 - "comsvcs/IComTransaction2Events.OnTransactionAbort2"
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IComTransaction2Events.OnTransactionAbort2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComTransaction2Events::OnTransactionAbort2


## -description


Generated when a transaction aborts.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/ns-comsvcs-__midl___midl_itf_autosvcs_0000_0013_0001">COMSVCSEVENTINFO</a> structure.


### -param guidTx [in]

The transaction identifier.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-icomtransaction2events">IComTransaction2Events</a>
 

 

