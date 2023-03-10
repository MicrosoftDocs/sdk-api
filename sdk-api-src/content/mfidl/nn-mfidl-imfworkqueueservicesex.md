---
UID: NN:mfidl.IMFWorkQueueServicesEx
title: IMFWorkQueueServicesEx (mfidl.h)
description: Extends the IMFWorkQueueServices interface.
helpviewer_keywords: ["IMFWorkQueueServicesEx","IMFWorkQueueServicesEx interface [Media Foundation]","IMFWorkQueueServicesEx interface [Media Foundation]","described","mf.imfworkqueueservicesex","mfidl/IMFWorkQueueServicesEx"]
old-location: mf\imfworkqueueservicesex.htm
tech.root: mf
ms.assetid: 12d4f0f4-9a6d-4782-b5ae-4add6608782a
ms.date: 12/05/2018
ms.keywords: IMFWorkQueueServicesEx, IMFWorkQueueServicesEx interface [Media Foundation], IMFWorkQueueServicesEx interface [Media Foundation],described, mf.imfworkqueueservicesex, mfidl/IMFWorkQueueServicesEx
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IMFWorkQueueServicesEx
 - mfidl/IMFWorkQueueServicesEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFWorkQueueServicesEx
---

# IMFWorkQueueServicesEx interface


## -description

Extends the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices">IMFWorkQueueServices</a> interface.

## -inheritance

The <b>IMFWorkQueueServicesEx</b> interface inherits from <b>IMFWorkQueueServices</b>. <b>IMFWorkQueueServicesEx</b> also has these types of members:

## -remarks

This interface allows applications to control
both platform and topology work queues.

The <a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices">IMFWorkQueueServices</a> can be obtained from the session by querying     for the <b>MF_WORKQUEUE_SERVICES</b> service.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
