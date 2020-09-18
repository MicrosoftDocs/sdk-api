---
UID: NN:appxpackaging.IAppxBundleManifestPackageInfo
title: IAppxBundleManifestPackageInfo (appxpackaging.h)
description: Provides a read-only object model for a &lt;Package&gt; element in a bundle package manifest.
helpviewer_keywords: ["IAppxBundleManifestPackageInfo","IAppxBundleManifestPackageInfo interface [App packaging and management]","IAppxBundleManifestPackageInfo interface [App packaging and management]","described","appxpackaging/IAppxBundleManifestPackageInfo","appxpkg.iappxbundlemanifestpackageinfo"]
old-location: appxpkg\iappxbundlemanifestpackageinfo.htm
tech.root: appxpkg
ms.assetid: B9272875-E02A-4443-82B3-C64104E8291C
ms.date: 12/05/2018
ms.keywords: IAppxBundleManifestPackageInfo, IAppxBundleManifestPackageInfo interface [App packaging and management], IAppxBundleManifestPackageInfo interface [App packaging and management],described, appxpackaging/IAppxBundleManifestPackageInfo, appxpkg.iappxbundlemanifestpackageinfo
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IAppxBundleManifestPackageInfo
 - appxpackaging/IAppxBundleManifestPackageInfo
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
 - IAppxBundleManifestPackageInfo
---

# IAppxBundleManifestPackageInfo interface


## -description

Provides a read-only object model for a &lt;Package&gt; element in a bundle package manifest.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBundleManifestPackageInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxBundleManifestPackageInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBundleManifestPackageInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlemanifestpackageinfo-getfilename">GetFileName</a>
</td>
<td align="left" width="63%">
Retrieves the file-name attribute of the package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlemanifestpackageinfo-getoffset">GetOffset</a>
</td>
<td align="left" width="63%">
Retrieves the offset of the package relative to the beginning of the bundle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlemanifestpackageinfo-getpackageid">GetPackageId</a>
</td>
<td align="left" width="63%">
Retrieves an object that represents the identity of the app package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlemanifestpackageinfo-getpackagetype">GetPackageType</a>
</td>
<td align="left" width="63%">
Retrieves the type of package that is represented by the package info.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlemanifestpackageinfo-getresources">GetResources</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator that iterates through all the &lt;Resource&gt; elements that are defined in the app package's manifest.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlemanifestpackageinfo-getsize">GetSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of the package, in bytes.

</td>
</tr>
</table>