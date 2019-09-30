---
UID: NN:wmcodecdsp.IWMCodecLeakyBucket
title: IWMCodecLeakyBucket (wmcodecdsp.h)
author: windows-sdk-content
description: Configures the &#0034;leaky bucket&#0034; parameters on a video encoder.
old-location: mf\iwmcodecleakybucketinterface.htm
tech.root: medfound
ms.assetid: 93a0169e-39fe-4152-8698-72a0650be41a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMCodecLeakyBucket, IWMCodecLeakyBucket interface [Media Foundation], IWMCodecLeakyBucket interface [Media Foundation],described, codecapi.iwmcodecleakybucketinterface, mf.iwmcodecleakybucketinterface, wmcodecdsp/IWMCodecLeakyBucket
ms.topic: interface
f1_keywords: 
 - "wmcodecdsp/IWMCodecLeakyBucket"
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - wmcodecdsp.h
api_name:
 - IWMCodecLeakyBucket
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMCodecLeakyBucket interface


## -description


Configures the "leaky bucket" parameters on a video encoder.

This interface is implemented by all of the encoder objects. You can get a pointer to the <b>IWMCodecLeakyBucket</b> interface for a Windows Media video encoder by calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> method of any other interface on the object, such as <a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject</a> or <a href="https://docs.microsoft.com/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a>. This interface is not  implemented on any of the decoders.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMCodecLeakyBucket</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMCodecLeakyBucket</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMCodecLeakyBucket</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecleakybucket-getbufferfullnessbits">GetBufferFullnessBits</a>
</td>
<td align="left" width="63%">
Not implemented in this release.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecleakybucket-getbuffersizebits">GetBufferSizeBits</a>
</td>
<td align="left" width="63%">
Retrieves the  current size of the buffer in bits.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecleakybucket-setbufferfullnessbits">SetBufferFullnessBits</a>
</td>
<td align="left" width="63%">
Not  implemented in this release.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecleakybucket-setbuffersizebits">SetBufferSizeBits</a>
</td>
<td align="left" width="63%">
Sets the buffer size in bits.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/the-leaky-bucket-buffer-model">The Leaky Bucket Buffer Model</a>
 

 

