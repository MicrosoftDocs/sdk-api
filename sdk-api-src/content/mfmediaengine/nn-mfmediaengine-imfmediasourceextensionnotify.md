---
UID: NN:mfmediaengine.IMFMediaSourceExtensionNotify
title: IMFMediaSourceExtensionNotify (mfmediaengine.h)
description: Provides functionality for raising events associated with IMFMediaSourceExtension.
old-location: mf\imfmediasourceextensionnotify.htm
tech.root: medfound
ms.assetid: 44eed02d-cf92-41e5-8748-1ce11ab4aac0
ms.date: 12/05/2018
ms.keywords: IMFMediaSourceExtensionNotify, IMFMediaSourceExtensionNotify interface [Media Foundation], IMFMediaSourceExtensionNotify interface [Media Foundation],described, mf.imfmediasourceextensionnotify, mfmediaengine/IMFMediaSourceExtensionNotify
ms.topic: interface
f1_keywords:
- mfmediaengine/IMFMediaSourceExtensionNotify
dev_langs:
- c++
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
- IMFMediaSourceExtensionNotify
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaSourceExtensionNotify interface


## -description


Provides functionality for raising events associated with <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension">IMFMediaSourceExtension</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaSourceExtensionNotify</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaSourceExtensionNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaSourceExtensionNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediasourceextensionnotify-onsourceclose">OnSourceClose</a>
</td>
<td align="left" width="63%">
Used to indicate that the media source has closed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediasourceextensionnotify-onsourceended">OnSourceEnded</a>
</td>
<td align="left" width="63%">
Used to indicate that the media source has ended.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediasourceextensionnotify-onsourceopen">OnSourceOpen</a>
</td>
<td align="left" width="63%">
Used to indicate that the  media source has opened.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

