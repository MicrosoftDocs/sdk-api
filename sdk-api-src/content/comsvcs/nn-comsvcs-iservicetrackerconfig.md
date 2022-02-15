---
UID: NN:comsvcs.IServiceTrackerConfig
title: IServiceTrackerConfig (comsvcs.h)
description: Configures the tracker property for the work that is done when calling either CoCreateActivity or CoEnterServiceDomain.
helpviewer_keywords: ["IServiceTrackerConfig","IServiceTrackerConfig interface [COM+]","IServiceTrackerConfig interface [COM+]","described","_cos_IServiceTrackerConfig","comsvcs/IServiceTrackerConfig","cos.iservicetrackerconfig"]
old-location: cos\iservicetrackerconfig.htm
tech.root: cos
ms.assetid: 342713d0-be5e-4d47-85ba-b18673a17fb5
ms.date: 12/05/2018
ms.keywords: IServiceTrackerConfig, IServiceTrackerConfig interface [COM+], IServiceTrackerConfig interface [COM+],described, _cos_IServiceTrackerConfig, comsvcs/IServiceTrackerConfig, cos.iservicetrackerconfig
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
 - IServiceTrackerConfig
 - comsvcs/IServiceTrackerConfig
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
 - IServiceTrackerConfig
---

# IServiceTrackerConfig interface


## -description

Configures the tracker property for the work that is done when calling either <a href="/windows/desktop/api/comsvcs/nf-comsvcs-cocreateactivity">CoCreateActivity</a> or <a href="/windows/desktop/api/comsvcs/nf-comsvcs-coenterservicedomain">CoEnterServiceDomain</a>.

## -inheritance

The <b>IServiceTrackerConfig</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IServiceTrackerConfig</b> also has these types of members:

## -remarks

The tracker property is a reporting mechanism used by monitoring code to watch which code is running when. It is the reporting mechanism behind the spinning balls in the Component Services administrative tool.

## -see-also

<a href="/windows/desktop/cossdk/cserviceconfig">CServiceConfig</a>
