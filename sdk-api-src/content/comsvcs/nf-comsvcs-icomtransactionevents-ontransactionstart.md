---
UID: NF:comsvcs.IComTransactionEvents.OnTransactionStart
title: IComTransactionEvents::OnTransactionStart (comsvcs.h)
description: Generated when a Microsoft Distributed Transaction Coordinator (DTC) transaction starts. (IComTransactionEvents.OnTransactionStart)
helpviewer_keywords: ["IComTransactionEvents interface [COM+]","OnTransactionStart method","IComTransactionEvents.OnTransactionStart","IComTransactionEvents::OnTransactionStart","OnTransactionStart","OnTransactionStart method [COM+]","OnTransactionStart method [COM+]","IComTransactionEvents interface","_dtc_IComTransactionEvents_OnTransactionStart","comsvcs/IComTransactionEvents::OnTransactionStart","cos.icomtransactionevents_ontransactionstart"]
old-location: cos\icomtransactionevents_ontransactionstart.htm
tech.root: cos
ms.assetid: ef9d7adc-69ed-4582-9ce7-c66c947d48a6
ms.date: 12/05/2018
ms.keywords: IComTransactionEvents interface [COM+],OnTransactionStart method, IComTransactionEvents.OnTransactionStart, IComTransactionEvents::OnTransactionStart, OnTransactionStart, OnTransactionStart method [COM+], OnTransactionStart method [COM+],IComTransactionEvents interface, _dtc_IComTransactionEvents_OnTransactionStart, comsvcs/IComTransactionEvents::OnTransactionStart, cos.icomtransactionevents_ontransactionstart
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IComTransactionEvents::OnTransactionStart
 - comsvcs/IComTransactionEvents::OnTransactionStart
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComTransactionEvents.OnTransactionStart
---

# IComTransactionEvents::OnTransactionStart


## -description

Generated when a Microsoft Distributed Transaction Coordinator (DTC) transaction starts.

## -parameters

### -param pInfo [in]

A pointer to a <a href="/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo">COMSVCSEVENTINFO</a> structure.

### -param guidTx [in]

The transaction identifier.

### -param tsid [in]

The transaction stream identifier; a unique identifier for correlation to objects.

### -param fRoot [in]

Indicates whether this is a root transaction.

## -returns

The user verifies the return values from this method.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomtransactionevents">IComTransactionEvents</a>
