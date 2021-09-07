---
UID: NN:mfidl.IMFWorkQueueServices
title: IMFWorkQueueServices (mfidl.h)
description: Controls the work queues created by the Media Session.
helpviewer_keywords: ["7a6ddb67-9a8c-408c-b750-4f3fd3ba0d7d","IMFWorkQueueServices","IMFWorkQueueServices interface [Media Foundation]","IMFWorkQueueServices interface [Media Foundation]","described","mf.imfworkqueueservices","mfidl/IMFWorkQueueServices"]
old-location: mf\imfworkqueueservices.htm
tech.root: mf
ms.assetid: 7a6ddb67-9a8c-408c-b750-4f3fd3ba0d7d
ms.date: 12/05/2018
ms.keywords: 7a6ddb67-9a8c-408c-b750-4f3fd3ba0d7d, IMFWorkQueueServices, IMFWorkQueueServices interface [Media Foundation], IMFWorkQueueServices interface [Media Foundation],described, mf.imfworkqueueservices, mfidl/IMFWorkQueueServices
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFWorkQueueServices
 - mfidl/IMFWorkQueueServices
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFWorkQueueServices
---

# IMFWorkQueueServices interface


## -description

Controls the work queues created by the <a href="/windows/desktop/medfound/media-session">Media Session</a>.

The Media Session exposes this interface as a service. To obtain a pointer to this interface, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a> on the Media Session with the service identifier MF_WORKQUEUE_SERVICES.

## -inheritance

The <b>IMFWorkQueueServices</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFWorkQueueServices</b> also has these types of members:

## -remarks

If the application is using the protected media path (PMP) session, the methods in this interface automatically marshal the calls to the PMP process.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
