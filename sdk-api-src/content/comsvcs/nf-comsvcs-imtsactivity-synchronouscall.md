---
UID: NF:comsvcs.IMTSActivity.SynchronousCall
title: IMTSActivity::SynchronousCall (comsvcs.h)
description: Performs the user-defined work synchronously. (IMTSActivity.SynchronousCall)
helpviewer_keywords: ["IMTSActivity interface [COM+]","SynchronousCall method","IMTSActivity.SynchronousCall","IMTSActivity::SynchronousCall","SynchronousCall","SynchronousCall method [COM+]","SynchronousCall method [COM+]","IMTSActivity interface","_cos_IMTSActivity_SynchronousCall","comsvcs/IMTSActivity::SynchronousCall","cos.imtsactivity_synchronouscall"]
old-location: cos\imtsactivity_synchronouscall.htm
tech.root: cos
ms.assetid: 4f69956b-fdb3-47c4-9a19-e9f39a8d5e06
ms.date: 12/05/2018
ms.keywords: IMTSActivity interface [COM+],SynchronousCall method, IMTSActivity.SynchronousCall, IMTSActivity::SynchronousCall, SynchronousCall, SynchronousCall method [COM+], SynchronousCall method [COM+],IMTSActivity interface, _cos_IMTSActivity_SynchronousCall, comsvcs/IMTSActivity::SynchronousCall, cos.imtsactivity_synchronouscall
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
 - IMTSActivity::SynchronousCall
 - comsvcs/IMTSActivity::SynchronousCall
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
 - IMTSActivity.SynchronousCall
---

# IMTSActivity::SynchronousCall


## -description

Performs the user-defined work synchronously.

## -parameters

### -param pCall [in]

A pointer to the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-imtscall">IMTSCall</a> interface that is used to implement the batch work.

## -returns

This method always returns the <b>HRESULT</b> returned by the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-imtscall-oncall">OnCall</a> method of the <a href="/windows/desktop/api/comsvcs/nn-comsvcs-imtscall">IMTSCall</a> interface.

## -remarks

The batch work that is run using this method runs in the context and thread apartment of the activity that was created by the call to <a href="/windows/desktop/api/comsvcs/nf-comsvcs-mtscreateactivity">MTSCreateActivity</a>.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-imtsactivity">IMTSActivity</a>
