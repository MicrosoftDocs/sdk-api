---
UID: NF:control.IDeferredCommand.Confidence
title: IDeferredCommand::Confidence (control.h)
description: The Confidence method retrieves a confidence value that indicates how likely it is for the command to be invoked at the requested time.
helpviewer_keywords: ["Confidence","Confidence method [DirectShow]","Confidence method [DirectShow]","IDeferredCommand interface","IDeferredCommand interface [DirectShow]","Confidence method","IDeferredCommand.Confidence","IDeferredCommand::Confidence","IDeferredCommandConfidence","control/IDeferredCommand::Confidence","dshow.ideferredcommand_confidence"]
old-location: dshow\ideferredcommand_confidence.htm
tech.root: dshow
ms.assetid: fb3e97a5-b9bc-4a72-9ee7-0a6292fad99d
ms.date: 4/26/2023
ms.keywords: Confidence, Confidence method [DirectShow], Confidence method [DirectShow],IDeferredCommand interface, IDeferredCommand interface [DirectShow],Confidence method, IDeferredCommand.Confidence, IDeferredCommand::Confidence, IDeferredCommandConfidence, control/IDeferredCommand::Confidence, dshow.ideferredcommand_confidence
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
 - IDeferredCommand::Confidence
 - control/IDeferredCommand::Confidence
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
 - IDeferredCommand.Confidence
---

# IDeferredCommand::Confidence


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Confidence</code> method retrieves a confidence value that indicates how likely it is for the command to be invoked at the requested time.



This method is not implemented and returns E_NOTIMPL.

## -parameters

### -param pConfidence

Receives the confidence level, on a scale of 0 to 100.

## -returns

Returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ideferredcommand">IDeferredCommand Interface</a>