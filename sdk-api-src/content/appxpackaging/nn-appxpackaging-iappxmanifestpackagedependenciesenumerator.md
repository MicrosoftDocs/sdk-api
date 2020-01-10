---
UID: NN:appxpackaging.IAppxManifestPackageDependenciesEnumerator
title: IAppxManifestPackageDependenciesEnumerator (appxpackaging.h)
description: Enumerates the package dependencies defined in the package manifest.
old-location: appxpkg\iappxmanifestpackagedependenciesenumerator.htm
tech.root: appxpkg
ms.assetid: A09709AE-301F-4457-8E02-1A88FB283A43
ms.date: 12/05/2018
ms.keywords: IAppxManifestPackageDependenciesEnumerator, IAppxManifestPackageDependenciesEnumerator interface [App packaging and management], IAppxManifestPackageDependenciesEnumerator interface [App packaging and management],described, appxpackaging/IAppxManifestPackageDependenciesEnumerator, appxpkg.iappxmanifestpackagedependenciesenumerator
f1_keywords:
- appxpackaging/IAppxManifestPackageDependenciesEnumerator
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
- IAppxManifestPackageDependenciesEnumerator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxManifestPackageDependenciesEnumerator interface


## -description


Enumerates  the package dependencies defined in the package manifest.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxManifestPackageDependenciesEnumerator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxManifestPackageDependenciesEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxManifestPackageDependenciesEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestpackagedependenciesenumerator-getcurrent">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the dependency package at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestpackagedependenciesenumerator-gethascurrent">GetHasCurrent</a>
</td>
<td align="left" width="63%">
Determines whether there is a package dependency at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestpackagedependenciesenumerator-movenext">MoveNext</a>
</td>
<td align="left" width="63%">
Advances the position of the enumerator to the next package dependency.

</td>
</tr>
</table> 


## -remarks



This object can be retrieved using the <a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getpackagedependencies">IAppxManifestReader::GetPackageDependencies</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestpackagedependency">IAppxManifestPackageDependency</a>
 

 

