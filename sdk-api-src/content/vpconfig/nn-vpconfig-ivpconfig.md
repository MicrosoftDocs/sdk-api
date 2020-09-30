---
UID: NN:vpconfig.IVPConfig
title: IVPConfig (vpconfig.h)
description: The IVPConfig interface must be implemented by any filter that wraps a hardware decoder with a video port.
helpviewer_keywords: ["IVPConfig","IVPConfig interface [DirectShow]","IVPConfig interface [DirectShow]","described","IVPConfigInterface","dshow.ivpconfig","vpconfig/IVPConfig"]
old-location: dshow\ivpconfig.htm
tech.root: dshow
ms.assetid: 2c0eb294-7e57-4d8d-98b1-57c3834279a0
ms.date: 12/05/2018
ms.keywords: IVPConfig, IVPConfig interface [DirectShow], IVPConfig interface [DirectShow],described, IVPConfigInterface, dshow.ivpconfig, vpconfig/IVPConfig
req.header: vpconfig.h
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
 - IVPConfig
 - vpconfig/IVPConfig
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
 - IVPConfig
---

# IVPConfig interface


## -description

The <b>IVPConfig</b> interface must be implemented by any filter that wraps a hardware decoder with a video port. This enables the <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a>, through its <a href="/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify">IVPNotify</a> interface, to set and retrieve configuration information on the video port regarding the video memory on the display adapter. This interface derives from <a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpbaseconfig">IVPBaseConfig</a>.

Applications never use this interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVPConfig</b> interface inherits from <a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpbaseconfig">IVPBaseConfig</a>. <b>IVPConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVPConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vpconfig/nf-vpconfig-ivpconfig-isvpdecimationallowed">IsVPDecimationAllowed</a>
</td>
<td align="left" width="63%">
Given the context, retrieves whether scaling at the video port is possible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/vpconfig/nf-vpconfig-ivpconfig-setscalingfactors">SetScalingFactors</a>
</td>
<td align="left" width="63%">
Sets the factors by which the decoder should scale the video stream.

</td>
</tr>
</table>

## -remarks

Include Dvp.h and Vptype.h before Vpconfig.h.

## -see-also

<a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpbaseconfig">IVPBaseConfig</a>



<a href="/windows/desktop/api/vpnotify/nn-vpnotify-ivpbasenotify">IVPBaseNotify</a>



<a href="/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2">IVPNotify2</a>