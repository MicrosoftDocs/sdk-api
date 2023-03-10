---
UID: NN:comsvcs.IComSecurityEvents
title: IComSecurityEvents (comsvcs.h)
description: Notifies the subscriber if the authentication of a method call succeeded or failed.
helpviewer_keywords: ["IComSecurityEvents","IComSecurityEvents interface [COM+]","IComSecurityEvents interface [COM+]","described","_dtc_IComSecurityEvents","comsvcs/IComSecurityEvents","cos.icomsecurityevents"]
old-location: cos\icomsecurityevents.htm
tech.root: cos
ms.assetid: 83366f18-8dd4-4c3d-8362-4fbcc4c33b95
ms.date: 12/05/2018
ms.keywords: IComSecurityEvents, IComSecurityEvents interface [COM+], IComSecurityEvents interface [COM+],described, _dtc_IComSecurityEvents, comsvcs/IComSecurityEvents, cos.icomsecurityevents
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
 - IComSecurityEvents
 - comsvcs/IComSecurityEvents
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
 - IComSecurityEvents
---

# IComSecurityEvents interface


## -description

Notifies the subscriber if the authentication of a method call succeeded or failed. The events are published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b>IComSecurityEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComSecurityEvents</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
