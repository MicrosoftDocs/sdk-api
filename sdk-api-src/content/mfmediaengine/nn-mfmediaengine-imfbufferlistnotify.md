---
UID: NN:mfmediaengine.IMFBufferListNotify
title: IMFBufferListNotify (mfmediaengine.h)
description: Enables IMFSourceBufferList object to notify its clients of important state changes.
helpviewer_keywords: ["IMFBufferListNotify","IMFBufferListNotify interface [Media Foundation]","IMFBufferListNotify interface [Media Foundation]","described","mf.imfbufferlistnotify","mfmediaengine/IMFBufferListNotify"]
old-location: mf\imfbufferlistnotify.htm
tech.root: mf
ms.assetid: 2a2705b4-fac3-4059-b2c9-c03efaa9c15e
ms.date: 12/05/2018
ms.keywords: IMFBufferListNotify, IMFBufferListNotify interface [Media Foundation], IMFBufferListNotify interface [Media Foundation],described, mf.imfbufferlistnotify, mfmediaengine/IMFBufferListNotify
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFBufferListNotify
 - mfmediaengine/IMFBufferListNotify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFBufferListNotify
---

# IMFBufferListNotify interface


## -description

Enables <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebufferlist">IMFSourceBufferList</a> object to notify its clients of important state changes.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFBufferListNotify</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFBufferListNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFBufferListNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfbufferlistnotify-onaddsourcebuffer">OnAddSourceBuffer</a>
</td>
<td align="left" width="63%">
Indicates that a <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer">IMFSourceBuffer</a> has been added.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfbufferlistnotify-onremovesourcebuffer">OnRemoveSourceBuffer</a>
</td>
<td align="left" width="63%">
Indicates that a <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer">IMFSourceBuffer</a> has been removed.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>

