---
UID: NN:mfobjects.IMFMuxStreamMediaTypeManager
title: IMFMuxStreamMediaTypeManager (mfobjects.h)
description: Enables the management of stream configurations for a multiplexed media source. A stream configuration defines a set of substreams that can be included the multiplexed output.
old-location: mf\imfmuxstreammediatypemanager.htm
tech.root: medfound
ms.assetid: BBDAEF1C-DFEC-4647-8B74-E2ABB25F87CC
ms.date: 12/05/2018
ms.keywords: IMFMuxStreamMediaTypeManager, IMFMuxStreamMediaTypeManager interface [Media Foundation], IMFMuxStreamMediaTypeManager interface [Media Foundation],described, mf.imfmuxstreammediatypemanager, mfobjects/IMFMuxStreamMediaTypeManager
ms.topic: interface
f1_keywords:
- mfobjects/IMFMuxStreamMediaTypeManager
dev_langs:
- c++
req.header: mfobjects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfplat.lib
- mfplat.dll
- mfplat.dll
- mfplat.dll.dll
api_name:
- IMFMuxStreamMediaTypeManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMuxStreamMediaTypeManager interface


## -description


Enables the management of stream configurations for a multiplexed media source. A stream configuration defines a set of substreams that can be included  the  multiplexed output.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMuxStreamMediaTypeManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMuxStreamMediaTypeManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMuxStreamMediaTypeManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmuxstreammediatypemanager-addstreamconfiguration">AddStreamConfiguration</a>
</td>
<td align="left" width="63%">
Registers a stream configuration, which defines a set of substreams that can be included  the  multiplexed output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmuxstreamattributesmanager-getattributes">GetAttributes</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> for the substream with the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmuxstreammediatypemanager-getmediatype">GetMediaType</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> of the substream with the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmuxstreammediatypemanager-getstreamconfiguration">GetStreamConfiguration</a>
</td>
<td align="left" width="63%">
Gets the stream configuration with the specified index, which defines a set of substreams that can be included  the  multiplexed output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmuxstreammediatypemanager-getstreamconfigurationcount">GetStreamConfigurationCount</a>
</td>
<td align="left" width="63%">
Gets the count of registered stream configurations, which define set of substreams that can be included  the  multiplexed output.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmuxstreamattributesmanager-getstreamcount">GetStreamCount</a>
</td>
<td align="left" width="63%">
Gets the count of substreams managed by the multiplexed media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmuxstreammediatypemanager-getstreamcount">GetStreamCount</a>
</td>
<td align="left" width="63%">
Gets the count of substreams managed by the multiplexed media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmuxstreammediatypemanager-removestreamconfiguration">RemoveStreamConfiguration</a>
</td>
<td align="left" width="63%">
Unregisters a stream configuration, which defines a set of substreams that can be included  the  multiplexed output.

</td>
</tr>
</table> 

