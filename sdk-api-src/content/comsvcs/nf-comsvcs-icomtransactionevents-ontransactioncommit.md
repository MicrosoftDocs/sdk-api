---
UID: NF:comsvcs.IComTransactionEvents.OnTransactionCommit
title: IComTransactionEvents::OnTransactionCommit
author: windows-sdk-content
description: Generated when a transaction commits.
old-location: cos\icomtransactionevents_ontransactioncommit.htm
tech.root: cossdk
ms.assetid: c86b8b07-3dd0-48b8-9119-cb438238fc50
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IComTransactionEvents interface [COM+],OnTransactionCommit method, IComTransactionEvents.OnTransactionCommit, IComTransactionEvents::OnTransactionCommit, OnTransactionCommit, OnTransactionCommit method [COM+], OnTransactionCommit method [COM+],IComTransactionEvents interface, _dtc_IComTransactionEvents_OnTransactionCommit, comsvcs/IComTransactionEvents::OnTransactionCommit, cos.icomtransactionevents_ontransactioncommit
ms.topic: method
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
 - IComTransactionEvents.OnTransactionCommit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComTransactionEvents::OnTransactionCommit


## -description


Generated when a transaction commits.


## -parameters




### -param pInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms688276(v=VS.85).aspx">COMSVCSEVENTINFO</a> structure.


### -param guidTx [in]

The transaction identifier.


## -returns



The user verifies the return values from this method.




## -see-also




<a href="https://msdn.microsoft.com/f28a0ef5-1c9a-4fdc-bb10-2c381f22f5e3">IComTransactionEvents</a>
 

 

