---
UID: NN:mfobjects.IMFDXGIBuffer
title: IMFDXGIBuffer (mfobjects.h)
description: Represents a buffer that contains a Microsoft DirectX Graphics Infrastructure (DXGI)surface.
helpviewer_keywords: ["IMFDXGIBuffer","IMFDXGIBuffer interface [Media Foundation]","IMFDXGIBuffer interface [Media Foundation]","described","mf.imfdxgibuffer","mfobjects/IMFDXGIBuffer"]
old-location: mf\imfdxgibuffer.htm
tech.root: mf
ms.assetid: 796D7755-275D-4A0B-A34F-5D34DCEC8AC7
ms.date: 12/05/2018
ms.keywords: IMFDXGIBuffer, IMFDXGIBuffer interface [Media Foundation], IMFDXGIBuffer interface [Media Foundation],described, mf.imfdxgibuffer, mfobjects/IMFDXGIBuffer
f1_keywords:
- mfobjects/IMFDXGIBuffer
dev_langs:
- c++
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfobjects.h
api_name:
- IMFDXGIBuffer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFDXGIBuffer interface


## -description


Represents a buffer that contains a Microsoft DirectX Graphics Infrastructure (DXGI)surface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFDXGIBuffer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFDXGIBuffer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFDXGIBuffer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgibuffer-getresource">GetResource</a>
</td>
<td align="left" width="63%">
Queries the DXGIsurface for an interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgibuffer-getsubresourceindex">GetSubresourceIndex</a>
</td>
<td align="left" width="63%">
Gets the index of the subresource that is associated with this media buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgibuffer-getunknown">GetUnknown</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer that was previously stored in the media buffer object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfdxgibuffer-setunknown">SetUnknown</a>
</td>
<td align="left" width="63%">
Stores an arbitrary <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer in the media buffer object.

</td>
</tr>
</table> 


## -remarks



To create a DXGImedia buffer, first create the DXGIsurface. Then call <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxgisurfacebuffer">MFCreateDXGISurfaceBuffer</a>. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

