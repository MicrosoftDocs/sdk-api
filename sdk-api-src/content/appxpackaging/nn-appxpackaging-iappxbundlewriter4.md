---
UID: NN:appxpackaging.IAppxBundleWriter4
title: IAppxBundleWriter4 (appxpackaging.h)
description: Provides a write-only object model for bundle packages.
helpviewer_keywords: ["IAppxBundleWriter4","IAppxBundleWriter4 interface [App packaging and management]","IAppxBundleWriter4 interface [App packaging and management]","described","appxpackaging/IAppxBundleWriter4","appxpkg.iappxbundlewriter4"]
old-location: appxpkg\iappxbundlewriter4.htm
tech.root: appxpkg
ms.assetid: 9BB81F38-8451-4D3B-B0B6-31AF3001AB17
ms.date: 12/05/2018
ms.keywords: IAppxBundleWriter4, IAppxBundleWriter4 interface [App packaging and management], IAppxBundleWriter4 interface [App packaging and management],described, appxpackaging/IAppxBundleWriter4, appxpkg.iappxbundlewriter4
f1_keywords:
- appxpackaging/IAppxBundleWriter4
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
- IAppxBundleWriter4
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxBundleWriter4 interface


## -description


Provides a write-only object model for bundle packages.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBundleWriter4</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxBundleWriter4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBundleWriter4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlewriter4-addexternalpackagereference">AddExternalPackageReference</a>
</td>
<td align="left" width="63%">
Adds a reference within the package bundle to an external app package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlewriter4-addpackagereference">AddPackageReference</a>
</td>
<td align="left" width="63%">
Adds a reference to an optional app package or a payload file within an app bundle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlewriter4-addpayloadpackage">AddPayloadPackage</a>
</td>
<td align="left" width="63%">
Adds a new app package to the bundle.

</td>
</tr>
</table> 

