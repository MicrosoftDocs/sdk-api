---
UID: NN:mfmediaengine.IMFMediaEngineSrcElementsEx
title: IMFMediaEngineSrcElementsEx (mfmediaengine.h)
author: windows-sdk-content
description: Extends the IMFMediaEngineSrcElements interface to provide additional capabilities.
old-location: mf\imfmediaenginesrcelementsex.htm
tech.root: medfound
ms.assetid: f15cb527-0f46-4887-9e02-835f0115bc5b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineSrcElementsEx, IMFMediaEngineSrcElementsEx interface [Media Foundation], IMFMediaEngineSrcElementsEx interface [Media Foundation],described, mf.imfmediaenginesrcelementsex, mfmediaengine/IMFMediaEngineSrcElementsEx
ms.topic: interface
f1_keywords: ["mfmediaengine/IMFMediaEngineSrcElementsEx"]
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
 - IMFMediaEngineSrcElementsEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineSrcElementsEx interface


## -description


Extends the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesrcelements">IMFMediaEngineSrcElements</a> interface to provide additional capabilities.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngineSrcElementsEx</b> interface inherits from <b>IMFMediaEngineSrcElements</b>. <b>IMFMediaEngineSrcElementsEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEngineSrcElementsEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginesrcelementsex-addelementex">AddElementEx</a>
</td>
<td align="left" width="63%">
Provides an enhanced version of <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginesrcelements-addelement">IMFMediaEngineSrcElements::AddElement</a> to add the key system intended to be used with content to an element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginesrcelementsex-getkeysystem">GetKeySystem</a>
</td>
<td align="left" width="63%">
Gets the key system for the given source element index.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

