---
UID: NN:mfmediaengine.IMFMediaEngineSupportsSourceTransfer
title: IMFMediaEngineSupportsSourceTransfer (mfmediaengine.h)
author: windows-sdk-content
description: Enables the media source to be transferred between the media engine and the sharing engine for Play To.
old-location: mf\imfmediaenginesupportssourcetransfer.htm
tech.root: medfound
ms.assetid: 8784dcc2-52f4-41d9-a0ae-3ea7a736b604
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineSupportsSourceTransfer, IMFMediaEngineSupportsSourceTransfer interface [Media Foundation], IMFMediaEngineSupportsSourceTransfer interface [Media Foundation],described, mf.imfmediaenginesupportssourcetransfer, mfmediaengine/IMFMediaEngineSupportsSourceTransfer
ms.topic: interface
f1_keywords: ["mfmediaengine/IMFMediaEngineSupportsSourceTransfer"]
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - mfmediaengine.h
api_name:
 - IMFMediaEngineSupportsSourceTransfer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineSupportsSourceTransfer interface


## -description


Enables the media source to be transferred between  the media engine and the sharing engine for Play To.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngineSupportsSourceTransfer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaEngineSupportsSourceTransfer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEngineSupportsSourceTransfer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginesupportssourcetransfer-attachmediasource">AttachMediaSource</a>
</td>
<td align="left" width="63%">
Attaches the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginesupportssourcetransfer-detachmediasource">DetachMediaSource</a>
</td>
<td align="left" width="63%">
Detaches the media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginesupportssourcetransfer-shouldtransfersource">ShouldTransferSource</a>
</td>
<td align="left" width="63%">
Specifies wether or not the source should be transferred.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

