---
UID: NN:appxpackaging.IAppxManifestMainPackageDependency
title: IAppxManifestMainPackageDependency (appxpackaging.h)
description: Provides access to attribute values of the main package dependency.
old-location: appxpkg\iappxmanifestmainpackagedependency.htm
tech.root: appxpkg
ms.assetid: E9B04DAD-BD45-4699-9EB1-99CF59F8D934
ms.date: 12/05/2018
ms.keywords: IAppxManifestMainPackageDependency, IAppxManifestMainPackageDependency interface [App packaging and management], IAppxManifestMainPackageDependency interface [App packaging and management],described, appxpackaging/IAppxManifestMainPackageDependency, appxpkg.iappxmanifestmainpackagedependency
f1_keywords:
- appxpackaging/IAppxManifestMainPackageDependency
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
- IAppxManifestMainPackageDependency
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxManifestMainPackageDependency interface


## -description


Provides access to attribute values of the main package dependency.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxManifestMainPackageDependency</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxManifestMainPackageDependency</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxManifestMainPackageDependency</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestmainpackagedependency-getname">GetName</a>
</td>
<td align="left" width="63%">
Gets the name of the main package dependency from the AppxManifest.xml.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestmainpackagedependency-getpackagefamilyname">GetPackageFamilyName</a>
</td>
<td align="left" width="63%">
Gets the package family name of the main package dependency from the AppxManifest.xml.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestmainpackagedependency-getpublisher">GetPublisher</a>
</td>
<td align="left" width="63%">
Gets the publisher of the main package dependency from the AppxManifest.xml.

</td>
</tr>
</table> 

