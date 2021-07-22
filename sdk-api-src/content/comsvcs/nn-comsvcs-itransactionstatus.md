---
UID: NN:comsvcs.ITransactionStatus
title: ITransactionStatus (comsvcs.h)
description: Used to discover the status of the transaction that is completed by the call to CoLeaveServiceDomain when CServiceConfig is configured to use transactions in the call to CoEnterServiceDomain.
helpviewer_keywords: ["ITransactionStatus","ITransactionStatus interface [COM+]","ITransactionStatus interface [COM+]","described","_cos_ITransactionStatus","comsvcs/ITransactionStatus","cos.itransactionstatus"]
old-location: cos\itransactionstatus.htm
tech.root: cos
ms.assetid: df5eba93-6db7-478c-b6d7-831c20398d66
ms.date: 12/05/2018
ms.keywords: ITransactionStatus, ITransactionStatus interface [COM+], ITransactionStatus interface [COM+],described, _cos_ITransactionStatus, comsvcs/ITransactionStatus, cos.itransactionstatus
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITransactionStatus
 - comsvcs/ITransactionStatus
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
 - ITransactionStatus
---

# ITransactionStatus interface


## -description

Used to discover the status of the transaction that is completed by the call to <a href="/windows/desktop/api/comsvcs/nf-comsvcs-coleaveservicedomain">CoLeaveServiceDomain</a> when <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a> is configured to use transactions in the call to <a href="/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a>.

## -inheritance

The <b>ITransactionStatus</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITransactionStatus</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--transactions">COM+ Transactions</a>



<a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-coleaveservicedomain">CoLeaveServiceDomain</a>
