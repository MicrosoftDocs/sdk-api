---
UID: NN:wmsecure.IWMAuthorizer
title: IWMAuthorizer (wmsecure.h)
description: Provides access to certificates.helpviewer_keywords: ["IWMAuthorizer","IWMAuthorizer interface [windows Media Format]","IWMAuthorizer interface [windows Media Format]","described","wmformat.iwmauthorizer","wmsecure/IWMAuthorizer"]
old-location: wmformat\iwmauthorizer.htm
tech.root: wmformat
ms.assetid: eece7e36-7c3e-4bc4-9b5a-8142a062dbce
ms.date: 12/05/2018
ms.keywords: IWMAuthorizer, IWMAuthorizer interface [windows Media Format], IWMAuthorizer interface [windows Media Format],described, wmformat.iwmauthorizer, wmsecure/IWMAuthorizer
f1_keywords:
- wmsecure/IWMAuthorizer
dev_langs:
- c++
req.header: wmsecure.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
- wmsecure.h
api_name:
- IWMAuthorizer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMAuthorizer interface


## -description


<p class="CCE_Message">[<b>IWMAuthorizer</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]

Provides access to certificates.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMAuthorizer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMAuthorizer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMAuthorizer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsecure/nf-wmsecure-iwmauthorizer-getcert">GetCert</a>
</td>
<td align="left" width="63%">
Retrieves the specified certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsecure/nf-wmsecure-iwmauthorizer-getcertcount">GetCertCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of certificates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsecure/nf-wmsecure-iwmauthorizer-getshareddata">GetSharedData</a>
</td>
<td align="left" width="63%">
Retrieves shared  data for the specified certificate.

</td>
</tr>
</table> 

