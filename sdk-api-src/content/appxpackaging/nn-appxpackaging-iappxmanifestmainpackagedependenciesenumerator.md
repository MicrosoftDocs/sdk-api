---
UID: NN:appxpackaging.IAppxManifestMainPackageDependenciesEnumerator
title: IAppxManifestMainPackageDependenciesEnumerator (appxpackaging.h)
description: Enumerates &lt;MainPackageDependency&gt; elements from an app manifest.
helpviewer_keywords: ["IAppxManifestMainPackageDependenciesEnumerator","IAppxManifestMainPackageDependenciesEnumerator interface [App packaging and management]","IAppxManifestMainPackageDependenciesEnumerator interface [App packaging and management]","described","appxpackaging/IAppxManifestMainPackageDependenciesEnumerator","appxpkg.iappxmanifestmainpackagedependenciesenumerator"]
old-location: appxpkg\iappxmanifestmainpackagedependenciesenumerator.htm
tech.root: appxpkg
ms.assetid: EB511040-5011-4B79-AFEE-DFF42E11025B
ms.date: 12/05/2018
ms.keywords: IAppxManifestMainPackageDependenciesEnumerator, IAppxManifestMainPackageDependenciesEnumerator interface [App packaging and management], IAppxManifestMainPackageDependenciesEnumerator interface [App packaging and management],described, appxpackaging/IAppxManifestMainPackageDependenciesEnumerator, appxpkg.iappxmanifestmainpackagedependenciesenumerator
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
 - IAppxManifestMainPackageDependenciesEnumerator
 - appxpackaging/IAppxManifestMainPackageDependenciesEnumerator
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
 - IAppxManifestMainPackageDependenciesEnumerator
---

# IAppxManifestMainPackageDependenciesEnumerator interface


## -description

Enumerates &lt;MainPackageDependency&gt; elements from an app manifest.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxManifestMainPackageDependenciesEnumerator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxManifestMainPackageDependenciesEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxManifestMainPackageDependenciesEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestmainpackagedependenciesenumerator-getcurrent">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the &lt;MainPackageDependency&gt; element at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestmainpackagedependenciesenumerator-gethascurrent">GetHasCurrent</a>
</td>
<td align="left" width="63%">
Determines whether there is a &lt;MainPackageDependency&gt; element at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestmainpackagedependenciesenumerator-movenext">MoveNext</a>
</td>
<td align="left" width="63%">
Advances the position of the enumerator to the next &lt;MainPackageDependency&gt; element.

</td>
</tr>
</table>

