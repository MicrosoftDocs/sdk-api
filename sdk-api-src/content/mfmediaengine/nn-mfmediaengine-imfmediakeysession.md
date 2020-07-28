---
UID: NN:mfmediaengine.IMFMediaKeySession
title: IMFMediaKeySession (mfmediaengine.h)
description: Represents a session with the Digital Rights Management (DRM) key system.
helpviewer_keywords: ["IMFMediaKeySession","IMFMediaKeySession interface [Media Foundation]","IMFMediaKeySession interface [Media Foundation]","described","mf.imfmediakeysession","mfmediaengine/IMFMediaKeySession"]
old-location: mf\imfmediakeysession.htm
tech.root: mf
ms.assetid: 07f97bc9-9da2-4655-9ab9-5e17abc57d6d
ms.date: 12/05/2018
ms.keywords: IMFMediaKeySession, IMFMediaKeySession interface [Media Foundation], IMFMediaKeySession interface [Media Foundation],described, mf.imfmediakeysession, mfmediaengine/IMFMediaKeySession
f1_keywords:
- mfmediaengine/IMFMediaKeySession
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
- IMFMediaKeySession
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaKeySession interface


## -description


Represents a session with the Digital Rights Management (DRM) key system.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaKeySession</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaKeySession</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaKeySession</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfmediakeysession-close">Close</a>
</td>
<td align="left" width="63%">
Closes the media key session and must be called before the key session is released.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeysession-get_keysystem">get_KeySystem</a>
</td>
<td align="left" width="63%">
Gets the name of the  key system name the media keys object was created with.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfmediakeysession-get-sessionid">get_SessionId</a>
</td>
<td align="left" width="63%">
Gets a unique session id created for this session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfmediakeysession-geterror">GetError</a>
</td>
<td align="left" width="63%">
Gets the error state associated with the media key session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfmediakeysession-update">Update</a>
</td>
<td align="left" width="63%">
Passes in a key value with any associated data required by the Content Decryption Module for the given key system.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

