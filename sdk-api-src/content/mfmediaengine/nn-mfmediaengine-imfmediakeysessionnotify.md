---
UID: NN:mfmediaengine.IMFMediaKeySessionNotify
title: IMFMediaKeySessionNotify (mfmediaengine.h)
description: Provides a mechanism for notifying the app about information regarding the media key session.
helpviewer_keywords: ["IMFMediaKeySessionNotify","IMFMediaKeySessionNotify interface [Media Foundation]","IMFMediaKeySessionNotify interface [Media Foundation]","described","mf.imfmediakeysessionnotify","mfmediaengine/IMFMediaKeySessionNotify"]
old-location: mf\imfmediakeysessionnotify.htm
tech.root: mf
ms.assetid: d28c16a8-4a74-40c3-be95-ff7e4b1cdc09
ms.date: 12/05/2018
ms.keywords: IMFMediaKeySessionNotify, IMFMediaKeySessionNotify interface [Media Foundation], IMFMediaKeySessionNotify interface [Media Foundation],described, mf.imfmediakeysessionnotify, mfmediaengine/IMFMediaKeySessionNotify
f1_keywords:
- mfmediaengine/IMFMediaKeySessionNotify
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
- IMFMediaKeySessionNotify
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaKeySessionNotify interface


## -description


Provides a mechanism for notifying the app about information regarding the media key session. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaKeySessionNotify</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaKeySessionNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaKeySessionNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyadded">KeyAdded</a>
</td>
<td align="left" width="63%">
Notifies the application that the key has been added.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keyerror">KeyError</a>
</td>
<td align="left" width="63%">
Notifies the application that an error occurred while processing the key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysessionnotify-keymessage">KeyMessage</a>
</td>
<td align="left" width="63%">
Passes information to the application so it can initiate a key acquisition.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

