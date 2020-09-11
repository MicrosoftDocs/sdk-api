---
UID: NN:comsvcs.IServiceSynchronizationConfig
title: IServiceSynchronizationConfig (comsvcs.h)
description: Configures the synchronization for the work that is done when calling either CoCreateActivity or CoEnterServiceDomain.
helpviewer_keywords: ["IServiceSynchronizationConfig","IServiceSynchronizationConfig interface [COM+]","IServiceSynchronizationConfig interface [COM+]","described","_cos_IServiceSynchronizationConfig","comsvcs/IServiceSynchronizationConfig","cos.iservicesynchronizationconfig"]
old-location: cos\iservicesynchronizationconfig.htm
tech.root: cos
ms.assetid: c4856738-66bf-4982-9440-83b72148c85c
ms.date: 12/05/2018
ms.keywords: IServiceSynchronizationConfig, IServiceSynchronizationConfig interface [COM+], IServiceSynchronizationConfig interface [COM+],described, _cos_IServiceSynchronizationConfig, comsvcs/IServiceSynchronizationConfig, cos.iservicesynchronizationconfig
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
 - IServiceSynchronizationConfig
 - comsvcs/IServiceSynchronizationConfig
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
 - IServiceSynchronizationConfig
---

# IServiceSynchronizationConfig interface


## -description

Configures the synchronization for the work that is done when calling either <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a> or <a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceSynchronizationConfig</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IServiceSynchronizationConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IServiceSynchronizationConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicesynchronizationconfig-configuresynchronization">ConfigureSynchronization</a>
</td>
<td align="left" width="63%">
Configures the synchronization for the enclosed work.


</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>

