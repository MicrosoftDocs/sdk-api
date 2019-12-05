---
UID: NN:vpnotify.IVPNotify
title: IVPNotify (vpnotify.h)
description: Supports a private communication mechanism between the Overlay Mixer filter and a VPE decoder filter that represents a hardware decoder.Only the Overlay Mixer filter implements this interface. Applications should never use it.
old-location: dshow\ivpnotify.htm
tech.root: DirectShow
ms.assetid: 6b40ba9e-8562-4d31-beaf-e4d4858bf145
ms.date: 12/05/2018
ms.keywords: IVPNotify, IVPNotify interface [DirectShow], IVPNotify interface [DirectShow],described, IVPNotifyInterface, dshow.ivpnotify, vpnotify/IVPNotify
ms.topic: interface
f1_keywords:
- vpnotify/IVPNotify
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVPNotify interface


## -description



Supports a private communication mechanism between the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter and a VPE decoder filter that represents a hardware decoder.

Only the Overlay Mixer filter implements this interface. Applications should never use it.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVPNotify</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/vpnotify/nn-vpnotify-ivpbasenotify">IVPBaseNotify</a>. <b>IVPNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVPNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vpnotify/nf-vpnotify-ivpnotify-getdeinterlacemode">GetDeinterlaceMode</a>
</td>
<td align="left" width="63%">
Retrieves the deinterlacing mode (such as bob or weave).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vpnotify/nf-vpnotify-ivpnotify-setdeinterlacemode">SetDeinterlaceMode</a>
</td>
<td align="left" width="63%">
Sets the deinterlacing mode (such as bob or weave).

</td>
</tr>
</table> 


## -remarks



Include Vptype.h before Vpnotify.h.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vpconfig/nn-vpconfig-ivpbaseconfig">IVPBaseConfig</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vpnotify/nn-vpnotify-ivpbasenotify">IVPBaseNotify</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vpconfig/nn-vpconfig-ivpconfig">IVPConfig</a>
 

 

