---
UID: NN:mfmediaengine.IMFMediaEngineNeedKeyNotify
title: IMFMediaEngineNeedKeyNotify (mfmediaengine.h)

description: Represents a callback to the media engine to notify key request data.
old-location: mf\imfmediaengineneedkeynotify.htm
tech.root: medfound
ms.assetid: bbedfbe8-9389-4b4f-8d52-111c787a6268

ms.date: 12/05/2018
ms.keywords: IMFMediaEngineNeedKeyNotify, IMFMediaEngineNeedKeyNotify interface [Media Foundation], IMFMediaEngineNeedKeyNotify interface [Media Foundation],described, mf.imfmediaengineneedkeynotify, mfmediaengine/IMFMediaEngineNeedKeyNotify
ms.topic: interface
f1_keywords: 
 - "mfmediaengine/IMFMediaEngineNeedKeyNotify"
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
 - IMFMediaEngineNeedKeyNotify
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineNeedKeyNotify interface


## -description


Represents a callback to the media engine to notify key request data.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngineNeedKeyNotify</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaEngineNeedKeyNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEngineNeedKeyNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineneedkeynotify-needkey">NeedKey</a>
</td>
<td align="left" width="63%">
Notifies the application that a key or keys are needed along with any initialization data.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

