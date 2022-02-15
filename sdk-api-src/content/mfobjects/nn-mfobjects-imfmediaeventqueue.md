---
UID: NN:mfobjects.IMFMediaEventQueue
title: IMFMediaEventQueue (mfobjects.h)
description: Provides an event queue for applications that need to implement the IMFMediaEventGenerator interface.
helpviewer_keywords: ["IMFMediaEventQueue","IMFMediaEventQueue interface [Media Foundation]","IMFMediaEventQueue interface [Media Foundation]","described","e1698caa-db70-436d-af6a-64c6e7247590","mf.imfmediaeventqueue","mfobjects/IMFMediaEventQueue"]
old-location: mf\imfmediaeventqueue.htm
tech.root: mf
ms.assetid: e1698caa-db70-436d-af6a-64c6e7247590
ms.date: 12/05/2018
ms.keywords: IMFMediaEventQueue, IMFMediaEventQueue interface [Media Foundation], IMFMediaEventQueue interface [Media Foundation],described, e1698caa-db70-436d-af6a-64c6e7247590, mf.imfmediaeventqueue, mfobjects/IMFMediaEventQueue
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
 - IMFMediaEventQueue
 - mfobjects/IMFMediaEventQueue
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
 - IMFMediaEventQueue
---

# IMFMediaEventQueue interface


## -description

Provides an event queue for applications that need to implement the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a> interface.

This interface is exposed by a helper object that implements an event queue. If you are writing a component that implements the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a> interface, you can use this object in your implementation. The event queue object is thread safe and provides methods to queue events and to pull them from the queue either synchronously or asynchronously. To create the event queue object, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue">MFCreateEventQueue</a>.

## -inheritance

The <b>IMFMediaEventQueue</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaEventQueue</b> also has these types of members:

## -remarks

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/media-event-generators">Media Event Generators</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
