---
UID: NN:mfobjects.IMFMediaEventGenerator
title: IMFMediaEventGenerator (mfobjects.h)
description: Retrieves events from any Media Foundation object that generates events.
helpviewer_keywords: ["IMFMediaEventGenerator","IMFMediaEventGenerator interface [Media Foundation]","IMFMediaEventGenerator interface [Media Foundation]","described","a37d0840-c896-43a0-b3d1-c2a6aaff1b25","mf.imfmediaeventgenerator","mfobjects/IMFMediaEventGenerator"]
old-location: mf\imfmediaeventgenerator.htm
tech.root: mf
ms.assetid: a37d0840-c896-43a0-b3d1-c2a6aaff1b25
ms.date: 12/05/2018
ms.keywords: IMFMediaEventGenerator, IMFMediaEventGenerator interface [Media Foundation], IMFMediaEventGenerator interface [Media Foundation],described, a37d0840-c896-43a0-b3d1-c2a6aaff1b25, mf.imfmediaeventgenerator, mfobjects/IMFMediaEventGenerator
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IMFMediaEventGenerator
 - mfobjects/IMFMediaEventGenerator
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
 - IMFMediaEventGenerator
---

# IMFMediaEventGenerator interface


## -description

Retrieves events from any Media Foundation object that generates events.

## -inheritance

The <b>IMFMediaEventGenerator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaEventGenerator</b> also has these types of members:

## -remarks

An object that supports this interface maintains a queue of events. The client of the object can retrieve the events either synchronously or asynchronously. The synchronous method is <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent">GetEvent</a>. The asynchronous methods are <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent">BeginGetEvent</a> and <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent">EndGetEvent</a>.

## -see-also

<a href="/windows/desktop/medfound/media-event-generators">Media Event Generators</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
