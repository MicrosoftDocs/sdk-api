---
UID: NN:appxpackaging.IAppxBundleWriter2
title: IAppxBundleWriter2 (appxpackaging.h)
description: Provides a write-only object model for bundle packages.
helpviewer_keywords: ["IAppxBundleWriter2","IAppxBundleWriter2 interface [App packaging and management]","IAppxBundleWriter2 interface [App packaging and management]","described","appxpackaging/IAppxBundleWriter2","appxpkg.iappxbundlewriter2"]
old-location: appxpkg\iappxbundlewriter2.htm
tech.root: appxpkg
ms.assetid: FD9EAF80-8449-4016-91A9-2299711C3D48
ms.date: 12/05/2018
ms.keywords: IAppxBundleWriter2, IAppxBundleWriter2 interface [App packaging and management], IAppxBundleWriter2 interface [App packaging and management],described, appxpackaging/IAppxBundleWriter2, appxpkg.iappxbundlewriter2
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
 - IAppxBundleWriter2
 - appxpackaging/IAppxBundleWriter2
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
 - IAppxBundleWriter2
---

# IAppxBundleWriter2 interface


## -description

Provides a write-only object model for bundle packages.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBundleWriter2</b> interface inherits from <a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlewriter">IAppxBundleWriter</a>. <b>IAppxBundleWriter2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBundleWriter2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlewriter2-addexternalpackagereference">AddExternalPackageReference</a>
</td>
<td align="left" width="63%">
Adds a reference to an external package to the package bundle.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlewriter">IAppxBundleWriter</a>