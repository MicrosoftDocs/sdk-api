---
UID: NN:comsvcs.IServiceActivity
title: IServiceActivity (comsvcs.h)
description: Used to call the batch work that is submitted through the activity created by CoCreateActivity.
helpviewer_keywords: ["IServiceActivity","IServiceActivity interface [COM+]","IServiceActivity interface [COM+]","described","_cos_IServiceActivity","comsvcs/IServiceActivity","cos.iserviceactivity"]
old-location: cos\iserviceactivity.htm
tech.root: cos
ms.assetid: 005bf0ec-f5a7-41a3-85b3-07f79f26af27
ms.date: 12/05/2018
ms.keywords: IServiceActivity, IServiceActivity interface [COM+], IServiceActivity interface [COM+],described, _cos_IServiceActivity, comsvcs/IServiceActivity, cos.iserviceactivity
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
 - IServiceActivity
 - comsvcs/IServiceActivity
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
 - IServiceActivity
---

# IServiceActivity interface


## -description

Used to call the batch work that is submitted through the activity created by <a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceActivity</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IServiceActivity</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IServiceActivity</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-iserviceactivity-asynchronouscall">AsynchronousCall</a>
</td>
<td align="left" width="63%">
Performs the user-defined work asynchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-iserviceactivity-bindtocurrentthread">BindToCurrentThread</a>
</td>
<td align="left" width="63%">
Binds the user-defined batch work to the current thread.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-iserviceactivity-synchronouscall">SynchronousCall</a>
</td>
<td align="left" width="63%">
Performs the user-defined work synchronously.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/comsvcs/nf-comsvcs-iserviceactivity-unbindfromthread">UnbindFromThread</a>
</td>
<td align="left" width="63%">
Unbinds the user-defined batch work from the thread on which it is running.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>



<a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iasyncerrornotify">IAsyncErrorNotify</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicecall">IServiceCall</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iservicethreadpoolconfig">IServiceThreadPoolConfig</a>