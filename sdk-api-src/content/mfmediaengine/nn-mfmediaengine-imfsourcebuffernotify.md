---
UID: NN:mfmediaengine.IMFSourceBufferNotify
title: IMFSourceBufferNotify (mfmediaengine.h)
author: windows-sdk-content
description: Provides functionality for raising events associated with IMFSourceBuffer.
old-location: mf\imfsourcebuffernotify.htm
tech.root: medfound
ms.assetid: 4a823d37-f55a-4810-aaed-4e04f5371d3b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFSourceBufferNotify, IMFSourceBufferNotify interface [Media Foundation], IMFSourceBufferNotify interface [Media Foundation],described, mf.imfsourcebuffernotify, mfmediaengine/IMFSourceBufferNotify
ms.topic: interface
f1_keywords: 
 - "mfmediaengine/IMFSourceBufferNotify"
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
 - IMFSourceBufferNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSourceBufferNotify interface


## -description


Provides functionality for raising events associated with <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer">IMFSourceBuffer</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSourceBufferNotify</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSourceBufferNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSourceBufferNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfsourcebuffernotify-onabort">OnAbort</a>
</td>
<td align="left" width="63%">
Used to indicate that the source buffer has been aborted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfsourcebuffernotify-onerror">OnError</a>
</td>
<td align="left" width="63%">
Used to indicate that an error has occurred with the  source buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfsourcebuffernotify-onupdate">OnUpdate</a>
</td>
<td align="left" width="63%">
Used to indicate that the source buffer is updating.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfsourcebuffernotify-onupdateend">OnUpdateEnd</a>
</td>
<td align="left" width="63%">
Used to indicate that the source buffer has finished updating.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfsourcebuffernotify-onupdatestart">OnUpdateStart</a>
</td>
<td align="left" width="63%">
Used to indicate that the source buffer has started updating.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

