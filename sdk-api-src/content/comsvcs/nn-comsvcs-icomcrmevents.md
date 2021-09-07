---
UID: NN:comsvcs.IComCRMEvents
title: IComCRMEvents (comsvcs.h)
description: Notifies the subscriber about activities of the Compensating Resource Manager (CRM) feature of Component Services.
helpviewer_keywords: ["IComCRMEvents","IComCRMEvents interface [COM+]","IComCRMEvents interface [COM+]","described","_dtc_icomcrmevents","comsvcs/IComCRMEvents","cos.icomcrmevents"]
old-location: cos\icomcrmevents.htm
tech.root: cos
ms.assetid: 720beffb-8fb5-4c87-9bcf-6db214543b01
ms.date: 12/05/2018
ms.keywords: IComCRMEvents, IComCRMEvents interface [COM+], IComCRMEvents interface [COM+],described, _dtc_icomcrmevents, comsvcs/IComCRMEvents, cos.icomcrmevents
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
 - IComCRMEvents
 - comsvcs/IComCRMEvents
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
 - IComCRMEvents
---

# IComCRMEvents interface


## -description

Notifies the subscriber about activities of the Compensating Resource Manager (CRM) feature of Component Services. The events are published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b>IComCRMEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComCRMEvents</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
