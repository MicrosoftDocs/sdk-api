---
UID: NN:mfidl.IMFPMPClientApp
title: IMFPMPClientApp (mfidl.h)
description: Provides a mechanism for a media source to implement content protection functionality in a Windows Store apps.
old-location: mf\imfpmpclientapp.htm
tech.root: medfound
ms.assetid: 03cd9e3c-65ac-40ad-802d-e36127dbd61f
ms.date: 12/05/2018
ms.keywords: IMFPMPClientApp, IMFPMPClientApp interface [Media Foundation], IMFPMPClientApp interface [Media Foundation],described, mf.imfpmpclientapp, mfidl/IMFPMPClientApp
f1_keywords:
- mfidl/IMFPMPClientApp
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfidl.h
api_name:
- IMFPMPClientApp
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPMPClientApp interface


## -description


Provides a mechanism for a media source to implement content protection functionality in a Windows Store apps.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFPMPClientApp</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFPMPClientApp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFPMPClientApp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfpmpclientapp-setpmphost">SetPMPHost</a>
</td>
<td align="left" width="63%">
Initialize the component with <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfpmphostapp">IMFPMPHostApp</a>.

</td>
</tr>
</table> 


## -remarks



<b>When to implement:</b> 
A media source implements <b>IMFPMPClientApp</b> in order to implement content protection functionality for Windows Store apps.






## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/pmp-media-session">PMP Media Session</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/protected-media-path">Protected Media Path</a>
 

 

