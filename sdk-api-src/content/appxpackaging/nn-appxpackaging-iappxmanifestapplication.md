---
UID: NN:appxpackaging.IAppxManifestApplication
title: IAppxManifestApplication (appxpackaging.h)
description: Provides access to attribute values of the application.
helpviewer_keywords: ["IAppxManifestApplication","IAppxManifestApplication interface [App packaging and management]","IAppxManifestApplication interface [App packaging and management]","described","appxpackaging/IAppxManifestApplication","appxpkg.iappxmanifestapplication"]
old-location: appxpkg\iappxmanifestapplication.htm
tech.root: appxpkg
ms.assetid: 16FC78D1-7387-4C90-9F63-BCFA110BC487
ms.date: 12/05/2018
ms.keywords: IAppxManifestApplication, IAppxManifestApplication interface [App packaging and management], IAppxManifestApplication interface [App packaging and management],described, appxpackaging/IAppxManifestApplication, appxpkg.iappxmanifestapplication
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAppxManifestApplication
 - appxpackaging/IAppxManifestApplication
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
 - IAppxManifestApplication
---

# IAppxManifestApplication interface


## -description

Provides access to attribute values of the application.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxManifestApplication</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxManifestApplication</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxManifestApplication</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestapplication-getappusermodelid">GetAppUserModelId</a>
</td>
<td align="left" width="63%">
Gets the application user model identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestapplication-getstringvalue">GetStringValue</a>
</td>
<td align="left" width="63%">
Gets the value of a string element in the application metadata section of the manifest.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestapplicationsenumerator">IAppxManifestApplicationsEnumerator</a>



<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader">IAppxManifestReader</a>