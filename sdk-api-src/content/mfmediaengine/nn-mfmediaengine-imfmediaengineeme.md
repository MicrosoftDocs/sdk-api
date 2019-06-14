---
UID: NN:mfmediaengine.IMFMediaEngineEME
title: IMFMediaEngineEME (mfmediaengine.h)
author: windows-sdk-content
description: Implemented by the media engine to add encrypted media extensions methods.
old-location: mf\imfmediaengineeme.htm
tech.root: medfound
ms.assetid: d03045d5-bafe-4e65-98da-e9ea8104c169
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineEME, IMFMediaEngineEME interface [Media Foundation], IMFMediaEngineEME interface [Media Foundation],described, mf.imfmediaengineeme, mfmediaengine/IMFMediaEngineEME
ms.topic: interface
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
 - IMFMediaEngineEME
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineEME interface


## -description


Implemented by the media engine to add encrypted media extensions methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngineEME</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaEngineEME</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEngineEME</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfmediaengineeme-get-keys">get_Keys</a>
</td>
<td align="left" width="63%">
Gets the media keys object associated with the media engine or <b>null</b> if there is not a media keys object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineeme-setmediakeys">SetMediaKeys</a>
</td>
<td align="left" width="63%">
Sets the media keys object to use with the media engine.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

