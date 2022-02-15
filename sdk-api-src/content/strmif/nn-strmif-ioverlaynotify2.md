---
UID: NN:strmif.IOverlayNotify2
title: IOverlayNotify2 (strmif.h)
description: The IOverlayNotify2 interface derives from the IOverlayNotify interface.
helpviewer_keywords: ["IOverlayNotify2","IOverlayNotify2 interface [DirectShow]","IOverlayNotify2 interface [DirectShow]","described","IOverlayNotify2Interface","dshow.ioverlaynotify2","strmif/IOverlayNotify2"]
old-location: dshow\ioverlaynotify2.htm
tech.root: dshow
ms.assetid: 439b3939-84da-48f5-b2a5-47f68fedef06
ms.date: 12/05/2018
ms.keywords: IOverlayNotify2, IOverlayNotify2 interface [DirectShow], IOverlayNotify2 interface [DirectShow],described, IOverlayNotify2Interface, dshow.ioverlaynotify2, strmif/IOverlayNotify2
req.header: strmif.h
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
 - IOverlayNotify2
 - strmif/IOverlayNotify2
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
 - IOverlayNotify2
---

# IOverlayNotify2 interface


## -description

The <code>IOverlayNotify2</code> interface derives from the <a href="/windows/desktop/api/strmif/nn-strmif-ioverlaynotify">IOverlayNotify</a> interface. <code>IOverlayNotify2</code> gives asynchronous notifications of changes to the rendering window, identifying changes to the exposed window area. The advise link optionally supports this for the purpose of accepting <a href="/windows/desktop/api/strmif/nf-strmif-ioverlaynotify2-ondisplaychange">IOverlayNotify2::OnDisplayChange</a> notification.

To get notifications that the exposed window area has changed, decoders that do their own drawing should implement an <code>IOverlayNotify2</code> interface.

The video renderer is the only filter that calls the method on this interface. This is done automatically by the default video renderer.

## -inheritance

The <b>IOverlayNotify2</b> interface inherits from <a href="/windows/desktop/api/strmif/nn-strmif-ioverlaynotify">IOverlayNotify</a>. <b>IOverlayNotify2</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/strmif/nn-strmif-ioverlaynotify">IOverlayNotify</a>
