---
UID: NN:comsvcs.IAsyncErrorNotify
title: IAsyncErrorNotify (comsvcs.h)
description: Used to implement error trapping on the asynchronous batch work that is submitted through the activity created by CoCreateActivity.
helpviewer_keywords: ["IAsyncErrorNotify","IAsyncErrorNotify interface [COM+]","IAsyncErrorNotify interface [COM+]","described","_cos_IAsyncErrorNotify","comsvcs/IAsyncErrorNotify","cos.iasyncerrornotify"]
old-location: cos\iasyncerrornotify.htm
tech.root: cos
ms.assetid: 870ab43a-c675-499b-a1e3-1f48176768c0
ms.date: 12/05/2018
ms.keywords: IAsyncErrorNotify, IAsyncErrorNotify interface [COM+], IAsyncErrorNotify interface [COM+],described, _cos_IAsyncErrorNotify, comsvcs/IAsyncErrorNotify, cos.iasyncerrornotify
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
 - IAsyncErrorNotify
 - comsvcs/IAsyncErrorNotify
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
 - IAsyncErrorNotify
---

# IAsyncErrorNotify interface


## -description

Used to implement error trapping on the asynchronous batch work that is submitted through the activity created by <a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>.

## -inheritance

The <b>IAsyncErrorNotify</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAsyncErrorNotify</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iserviceactivity">IServiceActivity</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicecall">IServiceCall</a>
