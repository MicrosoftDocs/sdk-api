---
UID: NN:vpnotify.IVPNotify2
title: IVPNotify2 (vpnotify.h)
description: The IVPNotify2 interface inherits from IVPNotify and is implemented by the Overlay Mixer filter.
helpviewer_keywords: ["IVPNotify2","IVPNotify2 interface [DirectShow]","IVPNotify2 interface [DirectShow]","described","IVPNotify2Interface","dshow.ivpnotify2","vpnotify/IVPNotify2"]
old-location: dshow\ivpnotify2.htm
tech.root: dshow
ms.assetid: 8d5fc7ee-93ee-4297-ba24-0eed63bec1ea
ms.date: 12/05/2018
ms.keywords: IVPNotify2, IVPNotify2 interface [DirectShow], IVPNotify2 interface [DirectShow],described, IVPNotify2Interface, dshow.ivpnotify2, vpnotify/IVPNotify2
req.header: vpnotify.h
req.include-header: 
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
 - IVPNotify2
 - vpnotify/IVPNotify2
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
 - IVPNotify2
---

# IVPNotify2 interface


## -description

The <code>IVPNotify2</code> interface inherits from <a href="/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify">IVPNotify</a> and is implemented by the <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter. This interface enables the Overlay Mixer to communicate with a video port (on a hardware device such as a decoder) that implements <a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpconfig">IVPConfig</a>.

Applications should never use this interface.

## -inheritance

The <b>IVPNotify2</b> interface inherits from <a href="/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify">IVPNotify</a>. <b>IVPNotify2</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

Include Vptype.h before Vpnotify.h.

## -see-also

<a href="/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify">IVPNotify</a>
