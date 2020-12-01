---
UID: NN:appxpackaging.IAppxEncryptedBundleWriter3
title: IAppxEncryptedBundleWriter3 (appxpackaging.h)
description: Provides a write-only object model for encrypted bundle packages.
helpviewer_keywords: ["IAppxEncryptedBundleWriter3","IAppxEncryptedBundleWriter3 interface [App packaging and management]","IAppxEncryptedBundleWriter3 interface [App packaging and management]","described","appxpackaging/IAppxEncryptedBundleWriter3","appxpkg.iappxencryptedbundlewriter3"]
old-location: appxpkg\iappxencryptedbundlewriter3.htm
tech.root: appxpkg
ms.assetid: 20394DB5-F8E3-43E0-B222-BC14E9D6C1CB
ms.date: 12/05/2018
ms.keywords: IAppxEncryptedBundleWriter3, IAppxEncryptedBundleWriter3 interface [App packaging and management], IAppxEncryptedBundleWriter3 interface [App packaging and management],described, appxpackaging/IAppxEncryptedBundleWriter3, appxpkg.iappxencryptedbundlewriter3
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAppxEncryptedBundleWriter3
 - appxpackaging/IAppxEncryptedBundleWriter3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxEncryptedBundleWriter3
---

# IAppxEncryptedBundleWriter3 interface


## -description

Provides a write-only object model for encrypted bundle packages.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxEncryptedBundleWriter3</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxEncryptedBundleWriter3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxEncryptedBundleWriter3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxencryptedbundlewriter3-addexternalpackagereference">AddExternalPackageReference</a>
</td>
<td align="left" width="63%">
Adds a reference within the encrypted package bundle to an external app package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxencryptedbundlewriter3-addpayloadpackageencrypted">AddPayloadPackageEncrypted</a>
</td>
<td align="left" width="63%">
Encrypts a new payload package to the bundle.

</td>
</tr>
</table>