---
UID: NN:comsvcs.IServiceInheritanceConfig
title: IServiceInheritanceConfig (comsvcs.h)
description: Determines whether to construct a new context based on the current context or to create a new context based solely on the information in CServiceConfig.
helpviewer_keywords: ["IServiceInheritanceConfig","IServiceInheritanceConfig interface [COM+]","IServiceInheritanceConfig interface [COM+]","described","_cos_IServiceInheritanceConfig","comsvcs/IServiceInheritanceConfig","cos.iserviceinheritanceconfig"]
old-location: cos\iserviceinheritanceconfig.htm
tech.root: cos
ms.assetid: 8bb95aef-7470-43cc-941d-2105cdf48f37
ms.date: 12/05/2018
ms.keywords: IServiceInheritanceConfig, IServiceInheritanceConfig interface [COM+], IServiceInheritanceConfig interface [COM+],described, _cos_IServiceInheritanceConfig, comsvcs/IServiceInheritanceConfig, cos.iserviceinheritanceconfig
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
 - IServiceInheritanceConfig
 - comsvcs/IServiceInheritanceConfig
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
 - IServiceInheritanceConfig
---

# IServiceInheritanceConfig interface


## -description

Determines whether to construct a new context based on the current context or to create a new context based solely on the information in <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>. A new context that is based on the current context can be modified by calls to the other interfaces of <a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>.

## -inheritance

The <b>IServiceInheritanceConfig</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IServiceInheritanceConfig</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>
