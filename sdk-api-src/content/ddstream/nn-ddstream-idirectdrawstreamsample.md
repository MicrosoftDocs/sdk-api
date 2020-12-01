---
UID: NN:ddstream.IDirectDrawStreamSample
title: IDirectDrawStreamSample (ddstream.h)
description: Note  This interface is deprecated.
helpviewer_keywords: ["IDirectDrawStreamSample","IDirectDrawStreamSample interface [DirectShow]","IDirectDrawStreamSample interface [DirectShow]","described","IDirectDrawStreamSampleInterface","ddstream/IDirectDrawStreamSample","dshow.idirectdrawstreamsample"]
old-location: dshow\idirectdrawstreamsample.htm
tech.root: dshow
ms.assetid: afc8ac84-4629-4c5d-b4b2-59c1eb1af35d
ms.date: 12/05/2018
ms.keywords: IDirectDrawStreamSample, IDirectDrawStreamSample interface [DirectShow], IDirectDrawStreamSample interface [DirectShow],described, IDirectDrawStreamSampleInterface, ddstream/IDirectDrawStreamSample, dshow.idirectdrawstreamsample
req.header: ddstream.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectDrawStreamSample
 - ddstream/IDirectDrawStreamSample
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ddstream.h
api_name:
 - IDirectDrawStreamSample
---

# IDirectDrawStreamSample interface


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IDirectDrawStreamSample</code> interface provides methods that set and retrieve pointers to the Microsoft DirectDraw surface associated with the current stream sample.

This interface isn't intended for implementation by application developers. It is exposed by sample objects created by the DirectDraw stream.

Use this interface when applications need to set clipping rectangles and retrieve the rendering surface for DirectDraw stream samples.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectDrawStreamSample</b> interface inherits from <a href="/windows/desktop/api/mmstream/nn-mmstream-istreamsample">IStreamSample</a>. <b>IDirectDrawStreamSample</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectDrawStreamSample</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/ddstream/nf-ddstream-idirectdrawstreamsample-getsurface">GetSurface</a>
</td>
<td align="left" width="63%">
Retrieves pointers to the current sample's DirectDraw surface and associated clipping rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/ddstream/nf-ddstream-idirectdrawstreamsample-setrect">SetRect</a>
</td>
<td align="left" width="63%">
Changes the clipping rectangle for a sample.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mmstream/nn-mmstream-istreamsample">IStreamSample</a>