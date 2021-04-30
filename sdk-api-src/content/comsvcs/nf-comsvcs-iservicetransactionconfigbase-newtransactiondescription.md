---
UID: NF:comsvcs.IServiceTransactionConfigBase.NewTransactionDescription
title: IServiceTransactionConfigBase::NewTransactionDescription (comsvcs.h)
description: Sets the name that is used when transaction statistics are displayed.
helpviewer_keywords: ["IServiceTransactionConfigBase interface [COM+]","NewTransactionDescription method","IServiceTransactionConfigBase.NewTransactionDescription","IServiceTransactionConfigBase::NewTransactionDescription","NewTransactionDescription","NewTransactionDescription method [COM+]","NewTransactionDescription method [COM+]","IServiceTransactionConfigBase interface","_cos_IServiceTransactionConfigBase_NewTransactionDescription","comsvcs/IServiceTransactionConfigBase::NewTransactionDescription","cos.iservicetransactionconfigbase_newtransactiondescription"]
old-location: cos\iservicetransactionconfigbase_newtransactiondescription.htm
tech.root: cos
ms.assetid: ecdc160b-168d-48f4-bbe3-46d654ee8607
ms.date: 12/05/2018
ms.keywords: IServiceTransactionConfigBase interface [COM+],NewTransactionDescription method, IServiceTransactionConfigBase.NewTransactionDescription, IServiceTransactionConfigBase::NewTransactionDescription, NewTransactionDescription, NewTransactionDescription method [COM+], NewTransactionDescription method [COM+],IServiceTransactionConfigBase interface, _cos_IServiceTransactionConfigBase_NewTransactionDescription, comsvcs/IServiceTransactionConfigBase::NewTransactionDescription, cos.iservicetransactionconfigbase_newtransactiondescription
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IServiceTransactionConfigBase::NewTransactionDescription
 - comsvcs/IServiceTransactionConfigBase::NewTransactionDescription
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
 - IServiceTransactionConfigBase.NewTransactionDescription
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

If you do not provide a description by using this method, the value of the <i>szTrackerCtxName</i> parameter from the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iservicetrackerconfig-trackerconfig">IServiceTrackerConfig::TrackerConfig</a> method is used to describe the transaction.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicetransactionconfigbase">IServiceTransactionConfigBase</a>