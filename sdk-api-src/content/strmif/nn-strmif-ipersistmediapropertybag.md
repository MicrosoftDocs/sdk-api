---
UID: NN:strmif.IPersistMediaPropertyBag
title: IPersistMediaPropertyBag (strmif.h)
description: The IPersistMediaPropertyBag interface sets and retrieves INFO and DISP chunks in Audio-Video Interleaved (AVI) streams.helpviewer_keywords: ["IPersistMediaPropertyBag","IPersistMediaPropertyBag interface [DirectShow]","IPersistMediaPropertyBag interface [DirectShow]","described","IPersistMediaPropertyBagInterface","dshow.ipersistmediapropertybag","strmif/IPersistMediaPropertyBag"]
old-location: dshow\ipersistmediapropertybag.htm
tech.root: DirectShow
ms.assetid: 33e4b76b-841a-4dc5-b117-e08a6f4dcbe7
ms.date: 12/05/2018
ms.keywords: IPersistMediaPropertyBag, IPersistMediaPropertyBag interface [DirectShow], IPersistMediaPropertyBag interface [DirectShow],described, IPersistMediaPropertyBagInterface, dshow.ipersistmediapropertybag, strmif/IPersistMediaPropertyBag
f1_keywords:
- strmif/IPersistMediaPropertyBag
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
- IPersistMediaPropertyBag
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPersistMediaPropertyBag interface


## -description



The <code>IPersistMediaPropertyBag</code> interface sets and retrieves INFO and DISP chunks in Audio-Video Interleaved (AVI) streams. It uses the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imediapropertybag">IMediaPropertyBag</a> interface to store the chunks as name/value pairs.

The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/avi-splitter-filter">AVI Splitter</a> filter and the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/wave-parser-filter">WAVE Parser</a> filter support this interface for reading INFO and DISP chunks from an AVI or WAV file. The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/avi-mux-filter">AVI Mux</a> filter supports the interface for writing these chunks into a file.

<code>IPersistMediaPropertyBag</code> is modeled after, but does not inherit from, the <b>IPersistPropertyBag</b> interface. For more information on <b>IPersistPropertyBag</b>, see the Platform SDK.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPersistMediaPropertyBag</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPersistMediaPropertyBag</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPersistMediaPropertyBag</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipersistmediapropertybag-initnew">InitNew</a>
</td>
<td align="left" width="63%">
Initializes the object to receive new properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipersistmediapropertybag-load">Load</a>
</td>
<td align="left" width="63%">
Loads properties from the media property bag into the filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipersistmediapropertybag-save">Save</a>
</td>
<td align="left" width="63%">
Saves properties from the filter into the media property bag.

</td>
</tr>
</table> 

