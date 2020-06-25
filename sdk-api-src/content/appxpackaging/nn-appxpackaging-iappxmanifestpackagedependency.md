---
UID: NN:appxpackaging.IAppxManifestPackageDependency
title: IAppxManifestPackageDependency (appxpackaging.h)
description: Describes the dependency of one package on another package.
helpviewer_keywords: ["IAppxManifestPackageDependency","IAppxManifestPackageDependency interface [App packaging and management]","IAppxManifestPackageDependency interface [App packaging and management]","described","appxpackaging/IAppxManifestPackageDependency","appxpkg.iappxmanifestpackagedependency"]
old-location: appxpkg\iappxmanifestpackagedependency.htm
tech.root: appxpkg
ms.assetid: 1A5515DA-4A9E-40EE-9AAC-F267DAE9DDBA
ms.date: 12/05/2018
ms.keywords: IAppxManifestPackageDependency, IAppxManifestPackageDependency interface [App packaging and management], IAppxManifestPackageDependency interface [App packaging and management],described, appxpackaging/IAppxManifestPackageDependency, appxpkg.iappxmanifestpackagedependency
f1_keywords:
- appxpackaging/IAppxManifestPackageDependency
dev_langs:
- c++
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
- IAppxManifestPackageDependency
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxManifestPackageDependency interface


## -description


Describes the dependency of one package on another package.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxManifestPackageDependency</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxManifestPackageDependency</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxManifestPackageDependency</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestpackagedependency-getminversion">GetMinVersion</a>
</td>
<td align="left" width="63%">
Gets the minimum version of the package on which the current package has a dependency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestpackagedependency-getname">GetName</a>
</td>
<td align="left" width="63%">
Gets the name of the package on which the current package has a dependency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestpackagedependency-getpublisher">GetPublisher</a>
</td>
<td align="left" width="63%">
Gets the name of the publisher that produced the package on which the current package depends.

</td>
</tr>
</table> 


## -remarks



A dependency package is a package that the current package depends on, as specified in the package manifest using the <a href="https://docs.microsoft.com/uwp/schemas/appxpackage/appxmanifestschema/element-packagedependency">PackageDependency</a> element.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestpackagedependenciesenumerator">IAppxManifestPackageDependenciesEnumerator</a>
 

 

