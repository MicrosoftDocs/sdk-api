---
UID: NN:mfidl.IMFPMPHostApp
title: IMFPMPHostApp (mfidl.h)
description: Allows a media source to create a Windows Runtime object in the Protected Media Path (PMP) process.
helpviewer_keywords: ["IMFPMPHostApp","IMFPMPHostApp interface [Media Foundation]","IMFPMPHostApp interface [Media Foundation]","described","mf.imfpmphostapp","mfidl/IMFPMPHostApp"]
old-location: mf\imfpmphostapp.htm
tech.root: mf
ms.assetid: ca24930d-bd1e-4c12-8246-1e505a98944a
ms.date: 12/05/2018
ms.keywords: IMFPMPHostApp, IMFPMPHostApp interface [Media Foundation], IMFPMPHostApp interface [Media Foundation],described, mf.imfpmphostapp, mfidl/IMFPMPHostApp
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IMFPMPHostApp
 - mfidl/IMFPMPHostApp
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFPMPHostApp
---

# IMFPMPHostApp interface


## -description

Allows a media source to create a <a href="https://docs.microsoft.com/windows/desktop/WinRT/reference">Windows Runtime</a> object in the <a href="https://docs.microsoft.com/windows/desktop/medfound/protected-media-path">Protected Media Path</a> (PMP) process.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFPMPHostApp</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFPMPHostApp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFPMPHostApp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpmphostapp-activateclassbyid">ActivateClassById</a>
</td>
<td align="left" width="63%">
Runtime class of the Windows Runtime object to create.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpmphostapp-lockprocess">LockProcess</a>
</td>
<td align="left" width="63%">
Blocks the PMP process from ending.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpmphostapp-unlockprocess">UnlockProcess</a>
</td>
<td align="left" width="63%">
Decrements the lock count on the PMP process.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/pmp-media-session">PMP Media Session</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/protected-media-path">Protected Media Path</a>

