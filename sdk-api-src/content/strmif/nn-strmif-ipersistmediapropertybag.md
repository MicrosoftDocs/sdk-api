---
UID: NN:strmif.IPersistMediaPropertyBag
title: IPersistMediaPropertyBag
author: windows-sdk-content
description: The IPersistMediaPropertyBag interface sets and retrieves INFO and DISP chunks in Audio-Video Interleaved (AVI) streams.
old-location: dshow\ipersistmediapropertybag.htm
tech.root: DirectShow
ms.assetid: 33e4b76b-841a-4dc5-b117-e08a6f4dcbe7
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IPersistMediaPropertyBag, IPersistMediaPropertyBag interface [DirectShow], IPersistMediaPropertyBag interface [DirectShow],described, IPersistMediaPropertyBagInterface, dshow.ipersistmediapropertybag, strmif/IPersistMediaPropertyBag
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPersistMediaPropertyBag interface


## -description



The <code>IPersistMediaPropertyBag</code> interface sets and retrieves INFO and DISP chunks in Audio-Video Interleaved (AVI) streams. It uses the <a href="https://msdn.microsoft.com/6f134160-b0aa-44fd-b1b9-938f11349eac">IMediaPropertyBag</a> interface to store the chunks as name/value pairs.

The <a href="https://msdn.microsoft.com/df3c7d11-7ecc-499a-af36-b74437e21999">AVI Splitter</a> filter and the <a href="https://msdn.microsoft.com/53a9538d-7a79-40bb-9468-d710eb238925">WAVE Parser</a> filter support this interface for reading INFO and DISP chunks from an AVI or WAV file. The <a href="https://msdn.microsoft.com/31d30c91-fc6a-45ec-a2e0-34e6a1e902a4">AVI Mux</a> filter supports the interface for writing these chunks into a file.

<code>IPersistMediaPropertyBag</code> is modeled after, but does not inherit from, the <b>IPersistPropertyBag</b> interface. For more information on <b>IPersistPropertyBag</b>, see the Platform SDK.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPersistMediaPropertyBag</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPersistMediaPropertyBag</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/46d51c05-b653-4f14-810a-eb49d33da359">InitNew</a>
</td>
<td align="left" width="63%">
Initializes the object to receive new properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02ee3911-0b85-404d-81c9-7d0e6b3ccd5d">Load</a>
</td>
<td align="left" width="63%">
Loads properties from the media property bag into the filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12c66650-31c1-40b8-9f3d-bc5553dbfa94">Save</a>
</td>
<td align="left" width="63%">
Saves properties from the filter into the media property bag.

</td>
</tr>
</table> 

