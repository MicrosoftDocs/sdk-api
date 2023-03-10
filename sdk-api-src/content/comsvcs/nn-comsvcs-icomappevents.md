---
UID: NN:comsvcs.IComAppEvents
title: IComAppEvents (comsvcs.h)
description: Notifies the subscriber if a COM+ server application is started, shut down, or forced to shut down.
helpviewer_keywords: ["IComAppEvents","IComAppEvents interface [COM+]","IComAppEvents interface [COM+]","described","_dtc_IComAppEvents","comsvcs/IComAppEvents","cos.icomappevents"]
old-location: cos\icomappevents.htm
tech.root: cos
ms.assetid: 61ae1926-601b-4d97-80e4-d2d2098ced39
ms.date: 12/05/2018
ms.keywords: IComAppEvents, IComAppEvents interface [COM+], IComAppEvents interface [COM+],described, _dtc_IComAppEvents, comsvcs/IComAppEvents, cos.icomappevents
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
 - IComAppEvents
 - comsvcs/IComAppEvents
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
 - IComAppEvents
---

# IComAppEvents interface


## -description

Notifies the subscriber if a COM+ server application is started, shut down, or forced to shut down.  The latter is initiated by the user calling a catalog method, such as <a href="/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog-shutdownapplication">ICOMAdminCatalog::ShutdownApplication</a>, to shut down the server. The events are published to the subscriber using the <a href="/windows/desktop/cossdk/com--events">COM+ Events</a> service, a loosely coupled events (LCE) system that stores event information from different publishers in an event store in the COM+ catalog.

## -inheritance

The <b>IComAppEvents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComAppEvents</b> also has these types of members:

## -see-also

<a href="/windows/desktop/cossdk/com--events">COM+ Events</a>



<a href="/windows/desktop/cossdk/com--instrumentation-concepts">COM+ Instrumentation</a>
