---
UID: NF:amvideo.IFullScreenVideoEx.SetMessageDrain
title: IFullScreenVideoEx::SetMessageDrain (amvideo.h)
description: The SetMessageDrain method specifies a window to receive mouse and keyboard messages from the video window.
helpviewer_keywords: ["IFullScreenVideoEx interface [DirectShow]","SetMessageDrain method","IFullScreenVideoEx.SetMessageDrain","IFullScreenVideoEx::SetMessageDrain","IFullScreenVideoSetMessageDrain","SetMessageDrain","SetMessageDrain method [DirectShow]","SetMessageDrain method [DirectShow]","IFullScreenVideoEx interface","amvideo/IFullScreenVideoEx::SetMessageDrain","dshow.ifullscreenvideoex_setmessagedrain"]
old-location: dshow\ifullscreenvideoex_setmessagedrain.htm
tech.root: dshow
ms.assetid: d0c24da9-c33f-48a7-b644-a7671acca20f
ms.date: 12/05/2018
ms.keywords: IFullScreenVideoEx interface [DirectShow],SetMessageDrain method, IFullScreenVideoEx.SetMessageDrain, IFullScreenVideoEx::SetMessageDrain, IFullScreenVideoSetMessageDrain, SetMessageDrain, SetMessageDrain method [DirectShow], SetMessageDrain method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::SetMessageDrain, dshow.ifullscreenvideoex_setmessagedrain
req.header: amvideo.h
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
 - IFullScreenVideoEx::SetMessageDrain
 - amvideo/IFullScreenVideoEx::SetMessageDrain
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
 - IFullScreenVideoEx.SetMessageDrain
---

# IFullScreenVideoEx::SetMessageDrain


## -description

The <code>SetMessageDrain</code> method specifies a window to receive mouse and keyboard messages from the video window.

## -parameters

### -param hwnd [in]

Specifies a handle to the message-drain window.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method is equivalent to the <a href="/windows/desktop/api/control/nf-control-ivideowindow-put_messagedrain">IVideoWindow::put_MessageDrain</a> method.

The Full Screen video renderer posts all mouse and keyboard messages to the window designated as a message drain. The exact list of messages that are posted is the same as the list given in <b>put_MessageDrain</b>.

Applications do not need to use this method. Instead, call the Filter Graph Manager's <b>put_MessageDrain</b> method before switching to full-screen mode. The Filter Graph Manager automatically sets the same message drain on the renderer that it selects for full-screen mode.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>