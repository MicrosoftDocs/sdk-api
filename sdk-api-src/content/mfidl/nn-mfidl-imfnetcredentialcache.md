---
UID: NN:mfidl.IMFNetCredentialCache
title: IMFNetCredentialCache (mfidl.h)
description: Gets credentials from the credential cache.
helpviewer_keywords: ["IMFNetCredentialCache","IMFNetCredentialCache interface [Media Foundation]","IMFNetCredentialCache interface [Media Foundation]","described","d02e26e7-e99c-4be7-8495-830eff2f1554","mf.imfnetcredentialcache","mfidl/IMFNetCredentialCache"]
old-location: mf\imfnetcredentialcache.htm
tech.root: mf
ms.assetid: d02e26e7-e99c-4be7-8495-830eff2f1554
ms.date: 12/05/2018
ms.keywords: IMFNetCredentialCache, IMFNetCredentialCache interface [Media Foundation], IMFNetCredentialCache interface [Media Foundation],described, d02e26e7-e99c-4be7-8495-830eff2f1554, mf.imfnetcredentialcache, mfidl/IMFNetCredentialCache
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFNetCredentialCache
 - mfidl/IMFNetCredentialCache
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFNetCredentialCache
---

# IMFNetCredentialCache interface


## -description

Gets credentials from the credential cache.

This interface is implemented by the credential cache object. Applications that implement the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager">IMFNetCredentialManager</a> interface can use this object to store the user's credentials. To create the credential cache object, call <a href="/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache">MFCreateCredentialCache</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFNetCredentialCache</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFNetCredentialCache</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFNetCredentialCache</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential">GetCredential</a>
</td>
<td align="left" width="63%">
Gets the credential object for the specified URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setgood">SetGood</a>
</td>
<td align="left" width="63%">
Specifies whether the credential object provided successfully passed the authentication challenge.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions">SetUserOptions</a>
</td>
<td align="left" width="63%">
Specifies how user credentials are persisted.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="/windows/desktop/medfound/network-source-authentication">Network Source Authentication</a>