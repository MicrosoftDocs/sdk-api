---
UID: NF:comsvcs.IServiceActivity.SynchronousCall
title: IServiceActivity::SynchronousCall (comsvcs.h)
description: Performs the user-defined work synchronously. (IServiceActivity.SynchronousCall)
helpviewer_keywords: ["IServiceActivity interface [COM+]","SynchronousCall method","IServiceActivity.SynchronousCall","IServiceActivity::SynchronousCall","SynchronousCall","SynchronousCall method [COM+]","SynchronousCall method [COM+]","IServiceActivity interface","_cos_IServiceActivity_SynchronousCall","comsvcs/IServiceActivity::SynchronousCall","cos.iserviceactivity_synchronouscall"]
old-location: cos\iserviceactivity_synchronouscall.htm
tech.root: cos
ms.assetid: d25e6942-7b1b-4b74-b711-2d0f513d0b38
ms.date: 12/05/2018
ms.keywords: IServiceActivity interface [COM+],SynchronousCall method, IServiceActivity.SynchronousCall, IServiceActivity::SynchronousCall, SynchronousCall, SynchronousCall method [COM+], SynchronousCall method [COM+],IServiceActivity interface, _cos_IServiceActivity_SynchronousCall, comsvcs/IServiceActivity::SynchronousCall, cos.iserviceactivity_synchronouscall
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
 - IServiceActivity::SynchronousCall
 - comsvcs/IServiceActivity::SynchronousCall
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
 - IServiceActivity.SynchronousCall
---

# IServiceActivity::SynchronousCall


## -description

Performs the user-defined work synchronously.

## -parameters

### -param pIServiceCall [in]

A pointer to the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicecall">IServiceCall</a> interface that is used to implement the batch work.

## -returns

This method always returns the <b>HRESULT</b> value returned by the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-iservicecall-oncall">OnCall</a> method of the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicecall">IServiceCall</a> interface.

## -remarks

The batch work that is run via this method runs in the context and thread apartment of the activity created by the call to <a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iserviceactivity">IServiceActivity</a>
