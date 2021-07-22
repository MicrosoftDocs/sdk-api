---
UID: NN:comsvcs.IComIdentityEvents
title: IComIdentityEvents (comsvcs.h)
description: Notifies the subscriber about an activity that is part of an Internet Information Services (IIS) Active Server Pages (ASP) page. For example, if a COM+ object is invoked in an ASP page, the user would be notified of this activity.
helpviewer_keywords: ["IComIdentityEvents","IComIdentityEvents interface [COM+]","IComIdentityEvents interface [COM+]","described","_dtc_IComIdentityEvents","comsvcs/IComIdentityEvents","cos.icomidentityevents"]
old-location: cos\icomidentityevents.htm
tech.root: cos
ms.assetid: f064a5cd-c84d-4b80-96fc-1036af333901
ms.date: 12/05/2018
ms.keywords: IComIdentityEvents, IComIdentityEvents interface [COM+], IComIdentityEvents interface [COM+],described, _dtc_IComIdentityEvents, comsvcs/IComIdentityEvents, cos.icomidentityevents
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
 - IComIdentityEvents
 - comsvcs/IComIdentityEvents
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
 - IComIdentityEvents
---

# IComIdentityEvents interface


## -description

Notifies the subscriber about an activity that is part of an Internet Information Services (IIS) Active Server Pages (ASP) page. For example, if a COM+ object is invoked in an ASP page, the user would be notified of this activity. The events are published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b>IComIdentityEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComIdentityEvents</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
