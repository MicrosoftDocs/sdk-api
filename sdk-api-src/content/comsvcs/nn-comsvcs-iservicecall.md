---
UID: NN:comsvcs.IServiceCall
title: IServiceCall (comsvcs.h)
description: Used to implement the batch work that is submitted through the activity created by CoCreateActivity.
old-location: cos\iservicecall.htm
tech.root: cossdk
ms.assetid: 97532e29-3d1a-4a7c-8103-dd7ae2866a70
ms.date: 12/05/2018
ms.keywords: IServiceCall, IServiceCall interface [COM+], IServiceCall interface [COM+],described, _cos_IServiceCall, comsvcs/IServiceCall, cos.iservicecall
ms.topic: interface
f1_keywords:
- comsvcs/IServiceCall
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
- IServiceCall
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IServiceCall interface


## -description


Used to implement the batch work that is submitted through the activity created by <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceCall</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IServiceCall</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IServiceCall</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicecall-oncall">OnCall</a>
</td>
<td align="left" width="63%">
Triggers the execution of the batch work implemented in this method.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iasyncerrornotify">IAsyncErrorNotify</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iserviceactivity">IServiceActivity</a>
 

 

