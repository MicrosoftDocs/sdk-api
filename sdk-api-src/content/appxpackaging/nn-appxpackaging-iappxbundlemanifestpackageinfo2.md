---
UID: NN:appxpackaging.IAppxBundleManifestPackageInfo2
title: IAppxBundleManifestPackageInfo2 (appxpackaging.h)
author: windows-sdk-content
description: Provides a read-only object model for a &lt;Package&gt; element in a bundle package manifest.
old-location: appxpkg\iappxbundlemanifestpackageinfo2.htm
tech.root: appxpkg
ms.assetid: 036CD1E1-F4D7-46B9-A287-2728BA45348A
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAppxBundleManifestPackageInfo2, IAppxBundleManifestPackageInfo2 interface [App packaging and management], IAppxBundleManifestPackageInfo2 interface [App packaging and management],described, appxpackaging/IAppxBundleManifestPackageInfo2, appxpkg.iappxbundlemanifestpackageinfo2
ms.topic: interface
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
 - IAppxBundleManifestPackageInfo2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxBundleManifestPackageInfo2 interface


## -description


Provides a read-only object model for a &lt;Package&gt; element in a bundle package manifest. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBundleManifestPackageInfo2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAppxBundleManifestPackageInfo2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBundleManifestPackageInfo2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0C1181F5-0BD9-4F8E-A4E3-75A562ADF56A">GetIsDefaultApplicablePackage</a>
</td>
<td align="left" width="63%">
Determines whether the app package is a default applicable package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C6AA5EE3-DE41-41DD-8804-70CDCA817C7A">GetIsNonQualifiedResourcePackage</a>
</td>
<td align="left" width="63%">
Determines whether the app package is a non-qualified resource package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0EAE15E9-5B23-43F4-B4C6-D75EC8D8F281">GetIsPackageReference</a>
</td>
<td align="left" width="63%">
Determines whether a package is stored inside an app bundle, or if it's a reference to a package.

</td>
</tr>
</table> 

