---
UID: NN:mfidl.IMFMediaSourceEx
title: IMFMediaSourceEx (mfidl.h)

description: Extends the IMFMediaSource interface to provide additional capabilities for a media source.
old-location: mf\imfmediasourceex.htm
tech.root: medfound
ms.assetid: C72C79D5-FD65-4F27-A8C8-B94BF5A9E829

ms.date: 12/05/2018
ms.keywords: IMFMediaSourceEx, IMFMediaSourceEx interface [Media Foundation], IMFMediaSourceEx interface [Media Foundation],described, mf.imfmediasourceex, mfidl/IMFMediaSourceEx
ms.topic: interface
f1_keywords: 
 - "mfidl/IMFMediaSourceEx"
dev_langs:
 - c++
req.header: mfidl.h
req.include-header: 
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
 - mfidl.h
api_name:
 - IMFMediaSourceEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaSourceEx interface


## -description


Extends the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a> interface to provide additional capabilities for a media source.

To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> on the media source. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaSourceEx</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a>. <b>IMFMediaSourceEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaSourceEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes">GetSourceAttributes</a>
</td>
<td align="left" width="63%">
Gets an attribute store for the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes">GetStreamAttributes</a>
</td>
<td align="left" width="63%">
Gets an attribute store for a stream on the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-setd3dmanager">SetD3DManager</a>
</td>
<td align="left" width="63%">
Sets a pointer to the DXGI Device Manager on the media source.

</td>
</tr>
</table> 


## -remarks



Implementations of this interface can return <b>E_NOTIMPL</b> for any methods that are not required by the media source.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

