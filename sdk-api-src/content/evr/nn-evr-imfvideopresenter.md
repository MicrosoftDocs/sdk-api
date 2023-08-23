---
UID: NN:evr.IMFVideoPresenter
title: IMFVideoPresenter (evr.h)
description: Represents a video presenter. A video presenter is an object that receives video frames, typically from a video mixer, and presents them in some way, typically by rendering them to the display.
helpviewer_keywords: ["8f6e3132-03e9-4a2e-9160-e39d29cf2408","IMFVideoPresenter","IMFVideoPresenter interface [Media Foundation]","IMFVideoPresenter interface [Media Foundation]","described","evr/IMFVideoPresenter","mf.imfvideopresenter"]
old-location: mf\imfvideopresenter.htm
tech.root: mfarchive
ms.assetid: 8f6e3132-03e9-4a2e-9160-e39d29cf2408
ms.date: 12/05/2018
ms.keywords: 8f6e3132-03e9-4a2e-9160-e39d29cf2408, IMFVideoPresenter, IMFVideoPresenter interface [Media Foundation], IMFVideoPresenter interface [Media Foundation],described, evr/IMFVideoPresenter, mf.imfvideopresenter
req.header: evr.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFVideoPresenter
 - evr/IMFVideoPresenter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoPresenter
archived: true
---

# IMFVideoPresenter interface


## -description

Represents a video presenter. A <i>video presenter</i> is an object that receives video frames, typically from a video mixer, and presents them in some way, typically by rendering them to the display. The enhanced video renderer (EVR) provides a default video presenter, and applications can implement custom presenters.

The video presenter receives video frames as soon as they are available from upstream. The video presenter is responsible for presenting frames at the correct time and for synchronizing with the presentation clock.

## -inheritance

The <b>IMFVideoPresenter</b> interface inherits from <a href="/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink">IMFClockStateSink</a>. <b>IMFVideoPresenter</b> also has these types of members:

## -see-also

<a href="/windows/desktop/medfound/how-to-write-an-evr-presenter">How to Write an EVR Presenter</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink">IMFClockStateSink</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
