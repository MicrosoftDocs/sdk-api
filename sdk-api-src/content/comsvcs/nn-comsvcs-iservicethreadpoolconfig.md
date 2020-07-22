---
UID: NN:comsvcs.IServiceThreadPoolConfig
title: IServiceThreadPoolConfig (comsvcs.h)
description: Configures the thread pool of the activity object that is returned by calling CoCreateActivity.
helpviewer_keywords: ["IServiceThreadPoolConfig","IServiceThreadPoolConfig interface [COM+]","IServiceThreadPoolConfig interface [COM+]","described","_cos_IServiceThreadPoolConfig","comsvcs/IServiceThreadPoolConfig","cos.iservicethreadpoolconfig"]
old-location: cos\iservicethreadpoolconfig.htm
tech.root: cos
ms.assetid: 89c04fef-c6a0-4d73-a25a-a70b4b0f0bcf
ms.date: 12/05/2018
ms.keywords: IServiceThreadPoolConfig, IServiceThreadPoolConfig interface [COM+], IServiceThreadPoolConfig interface [COM+],described, _cos_IServiceThreadPoolConfig, comsvcs/IServiceThreadPoolConfig, cos.iservicethreadpoolconfig
f1_keywords:
- comsvcs/IServiceThreadPoolConfig
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- ComSvcs.h
api_name:
- IServiceThreadPoolConfig
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IServiceThreadPoolConfig interface


## -description


Configures the thread pool of the activity object that is returned by calling <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a>. 



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceThreadPoolConfig</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IServiceThreadPoolConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IServiceThreadPoolConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicethreadpoolconfig-selectthreadpool">SelectThreadPool</a>
</td>
<td align="left" width="63%">
Selects the thread pool in which the work submitted through the activity is to run.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicethreadpoolconfig-setbindinginfo">SetBindingInfo</a>
</td>
<td align="left" width="63%">
Binds all work submitted by the activity to a single single-threaded apartment.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>
 

 

