---
UID: NN:appxpackaging.IAppxEncryptionFactory3
title: IAppxEncryptionFactory3 (appxpackaging.h)
author: windows-sdk-content
description: Creates objects for encrypting, decrypting, reading, and writing Windows app packages and bundles.
old-location: appxpkg\iappxencryptionfactory3.htm
tech.root: appxpkg
ms.assetid: ABF2F4BE-FC6A-4AF5-BD15-243ABFA055D9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAppxEncryptionFactory3, IAppxEncryptionFactory3 interface [App packaging and management], IAppxEncryptionFactory3 interface [App packaging and management],described, appxpackaging/IAppxEncryptionFactory3, appxpkg.iappxencryptionfactory3
ms.topic: interface
f1_keywords: 
 - "appxpackaging/IAppxEncryptionFactory3"
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
 - IAppxEncryptionFactory3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxEncryptionFactory3 interface


## -description


Creates objects for encrypting, decrypting,  reading, and writing Windows app packages and bundles.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxEncryptionFactory3</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxEncryptionFactory3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxEncryptionFactory3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxencryptionfactory3-createencryptedbundlewriter">CreateEncryptedBundleWriter</a>
</td>
<td align="left" width="63%">
Creates a write-only bundle object to which encrypted Windows app packages can be added.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxencryptionfactory3-createencryptedpackagewriter">CreateEncryptedPackageWriter</a>
</td>
<td align="left" width="63%">
Creates a new instance of an <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxencryptedpackagewriter">IAppxEncryptedPackageWriter</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxencryptionfactory3-encryptbundle">EncryptBundle</a>
</td>
<td align="left" width="63%">
Creates an encrypted Windows app bundle from an unencrypted one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxencryptionfactory3-encryptpackage">EncryptPackage</a>
</td>
<td align="left" width="63%">
Creates an encrypted Windows app package from an unencrypted one.

</td>
</tr>
</table> 

