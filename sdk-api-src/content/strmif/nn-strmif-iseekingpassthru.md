---
UID: NN:strmif.ISeekingPassThru
title: ISeekingPassThru (strmif.h)
description: The ISeekingPassThru interface creates a helper object that implements seeking for one-input filters.
old-location: dshow\iseekingpassthru.htm
tech.root: DirectShow
ms.assetid: a22f2723-b44e-4c7e-8508-db5c6af5b1d6
ms.date: 12/05/2018
ms.keywords: ISeekingPassThru, ISeekingPassThru interface [DirectShow], ISeekingPassThru interface [DirectShow],described, ISeekingPassThruInterface, dshow.iseekingpassthru, strmif/ISeekingPassThru
f1_keywords:
- strmif/ISeekingPassThru
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- ISeekingPassThru
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISeekingPassThru interface


## -description



The <code>ISeekingPassThru</code> interface creates a helper object that implements seeking for one-input filters. Filters can use this interface to implement the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imediaseeking">IMediaSeeking</a> and <a href="https://docs.microsoft.com/windows/desktop/api/control/nn-control-imediaposition">IMediaPosition</a> interfaces. For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/cpospassthru">CPosPassThru</a>.

Applications do not use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISeekingPassThru</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISeekingPassThru</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISeekingPassThru</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iseekingpassthru-init">Init</a>
</td>
<td align="left" width="63%">
Initializes the seeking helper object.

</td>
</tr>
</table> 


## -remarks



To obtain this interface, call <b>CoCreateInstance</b> with CLSID_SeekingPassThru. You can also use the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/createpospassthru">CreatePosPassThru</a> function in the base class library.



