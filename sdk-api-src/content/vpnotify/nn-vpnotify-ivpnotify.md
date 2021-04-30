---
UID: NN:vpnotify.IVPNotify
title: IVPNotify (vpnotify.h)
description: Supports a private communication mechanism between the Overlay Mixer filter and a VPE decoder filter that represents a hardware decoder.Only the Overlay Mixer filter implements this interface. Applications should never use it.
helpviewer_keywords: ["IVPNotify","IVPNotify interface [DirectShow]","IVPNotify interface [DirectShow]","described","IVPNotifyInterface","dshow.ivpnotify","vpnotify/IVPNotify"]
old-location: dshow\ivpnotify.htm
tech.root: dshow
ms.assetid: 6b40ba9e-8562-4d31-beaf-e4d4858bf145
ms.date: 12/05/2018
ms.keywords: IVPNotify, IVPNotify interface [DirectShow], IVPNotify interface [DirectShow],described, IVPNotifyInterface, dshow.ivpnotify, vpnotify/IVPNotify
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
 - IVPNotify
 - vpnotify/IVPNotify
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
 - IVPNotify
---

# IVPNotify interface


## -description

Supports a private communication mechanism between the <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter and a VPE decoder filter that represents a hardware decoder.

Only the Overlay Mixer filter implements this interface. Applications should never use it.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVPNotify</b> interface inherits from <a href="/windows/desktop/api/vpnotify/nn-vpnotify-ivpbasenotify">IVPBaseNotify</a>. <b>IVPNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -remarks

Include Vptype.h before Vpnotify.h.

## -see-also

<a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpbaseconfig">IVPBaseConfig</a>



<a href="/windows/desktop/api/vpnotify/nn-vpnotify-ivpbasenotify">IVPBaseNotify</a>



<a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpconfig">IVPConfig</a>
