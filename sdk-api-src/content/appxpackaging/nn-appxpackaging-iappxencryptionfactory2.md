---
UID: NN:appxpackaging.IAppxEncryptionFactory2
title: IAppxEncryptionFactory2 (appxpackaging.h)
description: Creates objects for encrypting, decrypting, reading, and writing Windows app packages and bundles.helpviewer_keywords: ["IAppxEncryptionFactory2","IAppxEncryptionFactory2 interface [App packaging and management]","IAppxEncryptionFactory2 interface [App packaging and management]","described","appxpackaging/IAppxEncryptionFactory2","appxpkg.iappxencryptionfactory2"]
old-location: appxpkg\iappxencryptionfactory2.htm
tech.root: appxpkg
ms.assetid: CEA749C5-1DD0-4207-83BA-905B8838A923
ms.date: 12/05/2018
ms.keywords: IAppxEncryptionFactory2, IAppxEncryptionFactory2 interface [App packaging and management], IAppxEncryptionFactory2 interface [App packaging and management],described, appxpackaging/IAppxEncryptionFactory2, appxpkg.iappxencryptionfactory2
f1_keywords:
- appxpackaging/IAppxEncryptionFactory2
dev_langs:
- c++
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
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
- AppxPackaging.h
api_name:
- IAppxEncryptionFactory2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxEncryptionFactory2 interface


## -description


Creates objects for encrypting, decrypting,  reading, and writing Windows app packages and bundles.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxEncryptionFactory2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxEncryptionFactory2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxEncryptionFactory2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxencryptionfactory2-createencryptedpackagewriter">CreateEncryptedPackageWriter</a>
</td>
<td align="left" width="63%">
Creates a new instance of an <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxencryptedpackagewriter">IAppxEncryptedPackageWriter</a>.

</td>
</tr>
</table> 

