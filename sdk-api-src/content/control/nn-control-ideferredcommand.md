---
UID: NN:control.IDeferredCommand
title: IDeferredCommand (control.h)
description: The IDeferredCommand interface cancels or modify graph-control commands that were queued using the IQueueCommand interface.When an application calls an IQueueCommand method on the Filter Graph Manager, it receives a pointer to the IDeferredCommand interface. The application can use the interface to cancel or postpone the command, or retrieve the return value from the command.
helpviewer_keywords: ["IDeferredCommand","IDeferredCommand interface [DirectShow]","IDeferredCommand interface [DirectShow]","described","IDeferredCommandInterface","control/IDeferredCommand","dshow.ideferredcommand"]
old-location: dshow\ideferredcommand.htm
tech.root: dshow
ms.assetid: 8161932a-16aa-4700-b91d-b4d8948ad59f
ms.date: 4/26/2023
ms.keywords: IDeferredCommand, IDeferredCommand interface [DirectShow], IDeferredCommand interface [DirectShow],described, IDeferredCommandInterface, control/IDeferredCommand, dshow.ideferredcommand
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
 - IDeferredCommand
 - control/IDeferredCommand
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
 - IDeferredCommand
---

# IDeferredCommand interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IDeferredCommand</code> interface cancels or modify graph-control commands that were queued using the <a href="/windows/desktop/api/control/nn-control-iqueuecommand">IQueueCommand</a> interface.

When an application calls an <b>IQueueCommand</b> method on the Filter Graph Manager, it receives a pointer to the <code>IDeferredCommand</code> interface. The application can use the interface to cancel or postpone the command, or retrieve the return value from the command.

## -inheritance

The <b>IDeferredCommand</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDeferredCommand</b> also has these types of members:

