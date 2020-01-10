---
UID: NN:comsvcs.IAsyncErrorNotify
title: IAsyncErrorNotify (comsvcs.h)
description: Used to implement error trapping on the asynchronous batch work that is submitted through the activity created by CoCreateActivity.
old-location: cos\iasyncerrornotify.htm
tech.root: cossdk
ms.assetid: 870ab43a-c675-499b-a1e3-1f48176768c0
ms.date: 12/05/2018
ms.keywords: IAsyncErrorNotify, IAsyncErrorNotify interface [COM+], IAsyncErrorNotify interface [COM+],described, _cos_IAsyncErrorNotify, comsvcs/IAsyncErrorNotify, cos.iasyncerrornotify
f1_keywords:
- comsvcs/IAsyncErrorNotify
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- ComSvcs.h
api_name:
- IAsyncErrorNotify
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAsyncErrorNotify interface


## -description


Used to implement error trapping on the asynchronous batch work that is submitted through the activity created by <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAsyncErrorNotify</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAsyncErrorNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAsyncErrorNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iasyncerrornotify-onerror">OnError</a>
</td>
<td align="left" width="63%">
Called by COM+ when an error occurs in your asynchronous batch work.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iserviceactivity">IServiceActivity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iservicecall">IServiceCall</a>
 

 

