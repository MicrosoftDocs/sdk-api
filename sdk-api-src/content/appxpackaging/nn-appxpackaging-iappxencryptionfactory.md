---
UID: NN:appxpackaging.IAppxEncryptionFactory
title: IAppxEncryptionFactory (appxpackaging.h)
description: Creates objects for encrypting, decrypting, reading, and writing packages and bundles.
old-location: appxpkg\iappxencryptionfactory.htm
tech.root: appxpkg
ms.assetid: F07138FE-340F-4493-A3A9-AED075B2CEEA
ms.date: 12/05/2018
ms.keywords: IAppxEncryptionFactory, IAppxEncryptionFactory interface [App packaging and management], IAppxEncryptionFactory interface [App packaging and management],described, appxpackaging/IAppxEncryptionFactory, appxpkg.iappxencryptionfactory
f1_keywords:
- appxpackaging/IAppxEncryptionFactory
dev_langs:
- c++
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
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
- IAppxEncryptionFactory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxEncryptionFactory interface


## -description


Creates objects for encrypting, decrypting,  reading, and writing packages and bundles.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxEncryptionFactory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxEncryptionFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxEncryptionFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxencryptionfactory-createencryptedbundlereader">CreateEncryptedBundleReader</a>
</td>
<td align="left" width="63%">
Creates a read-only bundle object to which encrypted Windows app packages can be added.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxencryptionfactory-createencryptedbundlewriter">CreateEncryptedBundleWriter</a>
</td>
<td align="left" width="63%">
Creates a write-only bundle object to which encrypted Windows app packages can be added.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxencryptionfactory-createencryptedpackagereader">CreateEncryptedPackageReader</a>
</td>
<td align="left" width="63%">
Creates a new instance of <b>IAppxEncryptedPackageReader</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxencryptionfactory-createencryptedpackagewriter">CreateEncryptedPackageWriter</a>
</td>
<td align="left" width="63%">
Creates a new instance of an <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxencryptedpackagewriter">IAppxEncryptedPackageWriter</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxencryptionfactory-decryptbundle">DecryptBundle</a>
</td>
<td align="left" width="63%">
Creates an unencrypted Windows app bundle from an encrypted one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxencryptionfactory-decryptpackage">DecryptPackage</a>
</td>
<td align="left" width="63%">
Creates an unencrypted Windows app package from an encrypted one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxencryptionfactory-encryptbundle">EncryptBundle</a>
</td>
<td align="left" width="63%">
Creates an encrypted Windows app bundle from an unencrypted one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxencryptionfactory-encryptpackage">EncryptPackage</a>
</td>
<td align="left" width="63%">
Creates an encrypted Windows app package from an unencrypted one.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxencryptedbundlewriter">IAppxEncryptedBundleWriter</a>



<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxencryptedpackagewriter">IAppxEncryptedPackageWriter</a>
 

 

