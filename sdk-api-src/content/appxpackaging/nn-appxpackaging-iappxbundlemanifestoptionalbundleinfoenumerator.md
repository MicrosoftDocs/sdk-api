---
UID: NN:appxpackaging.IAppxBundleManifestOptionalBundleInfoEnumerator
title: IAppxBundleManifestOptionalBundleInfoEnumerator (appxpackaging.h)

description: Enumerates the optional bundle information from a bundle.
old-location: appxpkg\iappxbundlemanifestoptionalbundleinfoenumerator.htm
tech.root: appxpkg
ms.assetid: 5BF38EC7-7C04-455B-AFAA-CC2A78E54A4F

ms.date: 12/05/2018
ms.keywords: IAppxBundleManifestOptionalBundleInfoEnumerator, IAppxBundleManifestOptionalBundleInfoEnumerator interface [App packaging and management], IAppxBundleManifestOptionalBundleInfoEnumerator interface [App packaging and management],described, appxpackaging/IAppxBundleManifestOptionalBundleInfoEnumerator, appxpkg.iappxbundlemanifestoptionalbundleinfoenumerator
ms.topic: interface
f1_keywords: 
 - "appxpackaging/IAppxBundleManifestOptionalBundleInfoEnumerator"
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
 - IAppxBundleManifestOptionalBundleInfoEnumerator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxBundleManifestOptionalBundleInfoEnumerator interface


## -description


Enumerates the optional bundle information from a bundle.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxBundleManifestOptionalBundleInfoEnumerator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxBundleManifestOptionalBundleInfoEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxBundleManifestOptionalBundleInfoEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlemanifestoptionalbundleinfoenumerator-getcurrent">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the optional bundle information at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlemanifestoptionalbundleinfoenumerator-gethascurrent">GetHasCurrent</a>
</td>
<td align="left" width="63%">
Determines whether there is optional bundle information at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlemanifestoptionalbundleinfoenumerator-movenext">MoveNext</a>
</td>
<td align="left" width="63%">
Advances the position of the enumerator to the next set of optional bundle information.

</td>
</tr>
</table> 

