---
UID: NN:comsvcs.IServiceComTIIntrinsicsConfig
title: IServiceComTIIntrinsicsConfig (comsvcs.h)
description: Configures the COM Transaction Integrator (COMTI) intrinsics for the work that is done when calling the CoCreateActivity or CoEnterServiceDomain function.
helpviewer_keywords: ["IServiceComTIIntrinsicsConfig","IServiceComTIIntrinsicsConfig interface [COM+]","IServiceComTIIntrinsicsConfig interface [COM+]","described","_cos_IServiceComTIIntrinsicsConfig","comsvcs/IServiceComTIIntrinsicsConfig","cos.iservicecomtiintrinsicsconfig"]
old-location: cos\iservicecomtiintrinsicsconfig.htm
tech.root: cos
ms.assetid: dafa74f9-21fb-4495-911a-60183d36d83c
ms.date: 12/05/2018
ms.keywords: IServiceComTIIntrinsicsConfig, IServiceComTIIntrinsicsConfig interface [COM+], IServiceComTIIntrinsicsConfig interface [COM+],described, _cos_IServiceComTIIntrinsicsConfig, comsvcs/IServiceComTIIntrinsicsConfig, cos.iservicecomtiintrinsicsconfig
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
 - IServiceComTIIntrinsicsConfig
 - comsvcs/IServiceComTIIntrinsicsConfig
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
 - IServiceComTIIntrinsicsConfig
---

# IServiceComTIIntrinsicsConfig interface


## -description

Configures the COM Transaction Integrator (COMTI) intrinsics for the work that is done when calling the <a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a> or <a href="/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a> function. The COMTI eases the task of wrapping mainframe transactions and business logic as COM components.

## -inheritance

The <b>IServiceComTIIntrinsicsConfig</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IServiceComTIIntrinsicsConfig</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>
