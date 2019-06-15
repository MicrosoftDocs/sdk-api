---
UID: NN:mfmediaengine.IMFSourceBufferList
title: IMFSourceBufferList (mfmediaengine.h)
author: windows-sdk-content
description: Represents a collection of IMFSourceBuffer objects.
old-location: mf\imfsourcebufferlist.htm
tech.root: medfound
ms.assetid: 26f66c2d-5f84-485f-bc86-c8399666c9f1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFSourceBufferList, IMFSourceBufferList interface [Media Foundation], IMFSourceBufferList interface [Media Foundation],described, mf.imfsourcebufferlist, mfmediaengine/IMFSourceBufferList
ms.topic: interface
f1_keywords: ["mfmediaengine/IMFSourceBufferList"]
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
 - IMFSourceBufferList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSourceBufferList interface


## -description


Represents a collection of <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer">IMFSourceBuffer</a> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSourceBufferList</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSourceBufferList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSourceBufferList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfsourcebufferlist-getlength">GetLength</a>
</td>
<td align="left" width="63%">
Gets the number of <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer">IMFSourceBuffer</a> objects  in the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfsourcebufferlist-getsourcebuffer">GetSourceBuffer</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer">IMFSourceBuffer</a> at the specified index in the list.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

