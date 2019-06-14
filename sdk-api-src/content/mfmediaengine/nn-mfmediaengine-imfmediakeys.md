---
UID: NN:mfmediaengine.IMFMediaKeys
title: IMFMediaKeys (mfmediaengine.h)
author: windows-sdk-content
description: Represents a media keys used for decrypting media data using a Digital Rights Management (DRM) key system.
old-location: mf\imfmediakeys.htm
tech.root: medfound
ms.assetid: 0689d938-e0be-46d7-bfed-add431331a90
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFMediaKeys, IMFMediaKeys interface [Media Foundation], IMFMediaKeys interface [Media Foundation],described, mf.imfmediakeys, mfmediaengine/IMFMediaKeys
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
 - IMFMediaKeys
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaKeys interface


## -description


Represents a media keys used for decrypting media data using a Digital Rights Management (DRM) key system. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaKeys</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaKeys</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaKeys</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfmediakeys-createsession">CreateSession</a>
</td>
<td align="left" width="63%">
Creates a media key session object using the specified initialization data and custom data.
.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeys-get_keysystem">get_KeySystem</a>
</td>
<td align="left" width="63%">
Gets the key system string the <b>IMFMediaKeys</b> object was created with.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediakeys-getsuspendnotify">GetSuspendNotify</a>
</td>
<td align="left" width="63%">
Gets the suspend notify interface of the Content Decryption Module (CDM).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/medfound/imfmediakeys-shutdown">Shutdown</a>
</td>
<td align="left" width="63%">


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

