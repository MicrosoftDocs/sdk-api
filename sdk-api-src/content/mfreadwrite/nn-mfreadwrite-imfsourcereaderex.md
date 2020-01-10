---
UID: NN:mfreadwrite.IMFSourceReaderEx
title: IMFSourceReaderEx (mfreadwrite.h)
description: Extends the IMFSourceReader interface.
old-location: mf\imfsourcereaderex.htm
tech.root: medfound
ms.assetid: 59888F9B-C464-4045-AA77-03EE16E2B598
ms.date: 12/05/2018
ms.keywords: IMFSourceReaderEx, IMFSourceReaderEx interface [Media Foundation], IMFSourceReaderEx interface [Media Foundation],described, mf.imfsourcereaderex, mfreadwrite/IMFSourceReaderEx
f1_keywords:
- mfreadwrite/IMFSourceReaderEx
dev_langs:
- c++
req.header: mfreadwrite.h
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
- mfreadwrite.h
api_name:
- IMFSourceReaderEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSourceReaderEx interface


## -description


Extends the <a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader">IMFSourceReader</a> interface.

The <a href="https://docs.microsoft.com/windows/desktop/medfound/source-reader">Source Reader</a> implements this interface in Windows 8. To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> on the Source Reader.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSourceReaderEx</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader">IMFSourceReader</a>. <b>IMFSourceReaderEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSourceReaderEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereaderex-addtransformforstream">AddTransformForStream</a>
</td>
<td align="left" width="63%">
Adds a transform, such as an audio or video effect, to a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereaderex-gettransformforstream">GetTransformForStream</a>
</td>
<td align="left" width="63%">
Gets a pointer to a Media Foundation transform (MFT) for a specified stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereaderex-removealltransformsforstream">RemoveAllTransformsForStream</a>
</td>
<td align="left" width="63%">
Removes all of the Media Foundation transforms (MFTs) for a specified stream, with the exception of the decoder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereaderex-setnativemediatype">SetNativeMediaType</a>
</td>
<td align="left" width="63%">
Sets the native media type for a stream on the media source.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader">IMFSourceReader</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/source-reader">Source Reader</a>
 

 

