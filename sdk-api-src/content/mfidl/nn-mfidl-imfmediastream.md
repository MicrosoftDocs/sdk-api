---
UID: NN:mfidl.IMFMediaStream
title: IMFMediaStream (mfidl.h)
description: Represents one stream in a media source.
helpviewer_keywords: ["66d07292-3bfe-4e68-b26f-890996262b98","IMFMediaStream","IMFMediaStream interface [Media Foundation]","IMFMediaStream interface [Media Foundation]","described","mf.imfmediastream","mfidl/IMFMediaStream"]
old-location: mf\imfmediastream.htm
tech.root: mf
ms.assetid: 66d07292-3bfe-4e68-b26f-890996262b98
ms.date: 12/05/2018
ms.keywords: 66d07292-3bfe-4e68-b26f-890996262b98, IMFMediaStream, IMFMediaStream interface [Media Foundation], IMFMediaStream interface [Media Foundation],described, mf.imfmediastream, mfidl/IMFMediaStream
req.header: mfidl.h
req.include-header: 
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
 - IMFMediaStream
 - mfidl/IMFMediaStream
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
 - IMFMediaStream
---

# IMFMediaStream interface


## -description

Represents one stream in a media source.

## -inheritance

The <b>IMFMediaStream</b> interface inherits from <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a>. <b>IMFMediaStream</b> also has these types of members:

## -remarks

Streams are created when a media source is started. For each stream, the media source sends an <a href="/windows/desktop/medfound/menewstream">MENewStream</a> event with a pointer to the stream's <b>IMFMediaStream</b> interface.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator">IMFMediaEventGenerator</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/media-sources">Media Sources</a>
