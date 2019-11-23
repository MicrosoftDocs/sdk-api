---
UID: NN:vpnotify.IVPNotify2
title: IVPNotify2 (vpnotify.h)

description: The IVPNotify2 interface inherits from IVPNotify and is implemented by the Overlay Mixer filter.
old-location: dshow\ivpnotify2.htm
tech.root: DirectShow
ms.assetid: 8d5fc7ee-93ee-4297-ba24-0eed63bec1ea

ms.date: 12/05/2018
ms.keywords: IVPNotify2, IVPNotify2 interface [DirectShow], IVPNotify2 interface [DirectShow],described, IVPNotify2Interface, dshow.ivpnotify2, vpnotify/IVPNotify2
ms.topic: interface
f1_keywords: 
 - "vpnotify/IVPNotify2"
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
 - IVPNotify2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVPNotify2 interface


## -description



The <code>IVPNotify2</code> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify">IVPNotify</a> and is implemented by the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter. This interface enables the Overlay Mixer to communicate with a video port (on a hardware device such as a decoder) that implements <a href="https://docs.microsoft.com/windows/desktop/api/vpconfig/nn-vpconfig-ivpconfig">IVPConfig</a>.

Applications should never use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVPNotify2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify">IVPNotify</a>. <b>IVPNotify2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVPNotify2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vpnotify/nf-vpnotify-ivpnotify2-getvpsyncmaster">GetVPSyncMaster</a>
</td>
<td align="left" width="63%">
Checks whether the video port controls the synchronization of the VGA.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vpnotify/nf-vpnotify-ivpnotify2-setvpsyncmaster">SetVPSyncMaster</a>
</td>
<td align="left" width="63%">
Sets whether the video port controls vertical synchronization of the VGA.

</td>
</tr>
</table> 


## -remarks



Include Vptype.h before Vpnotify.h.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify">IVPNotify</a>
 

 

