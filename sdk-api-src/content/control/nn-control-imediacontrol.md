---
UID: NN:control.IMediaControl
title: IMediaControl (control.h)
description: The IMediaControl interface provides methods for controlling the flow of data through the filter graph.
helpviewer_keywords: ["IMediaControl","IMediaControl interface [DirectShow]","IMediaControl interface [DirectShow]","described","IMediaControlInterface","control/IMediaControl","dshow.imediacontrol"]
old-location: dshow\imediacontrol.htm
tech.root: dshow
ms.assetid: bce64088-3751-420c-b9de-b9b5f3119198
ms.date: 4/26/2023
ms.keywords: IMediaControl, IMediaControl interface [DirectShow], IMediaControl interface [DirectShow],described, IMediaControlInterface, control/IMediaControl, dshow.imediacontrol
req.header: control.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaControl
 - control/IMediaControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMediaControl
---

# IMediaControl interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IMediaControl</code> interface provides methods for controlling the flow of data through the filter graph. It includes methods for running, pausing, and stopping the graph. The Filter Graph Manager implements this interface. For more information on filter graph states, see <a href="/windows/desktop/DirectShow/data-flow-in-the-filter-graph">Data Flow in the Filter Graph</a>.

## -inheritance

The <b>IMediaControl</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMediaControl</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
