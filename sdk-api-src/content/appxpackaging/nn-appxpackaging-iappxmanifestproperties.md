---
UID: NN:appxpackaging.IAppxManifestProperties
title: IAppxManifestProperties (appxpackaging.h)
description: Provides read-only access to the properties section of a package manifest.
helpviewer_keywords: ["IAppxManifestProperties","IAppxManifestProperties interface [App packaging and management]","IAppxManifestProperties interface [App packaging and management]","described","appxpackaging/IAppxManifestProperties","appxpkg.iappxmanifestproperties"]
old-location: appxpkg\iappxmanifestproperties.htm
tech.root: appxpkg
ms.assetid: 5DA0A805-13D3-4977-8EFB-45E8B51AAF60
ms.date: 12/05/2018
ms.keywords: IAppxManifestProperties, IAppxManifestProperties interface [App packaging and management], IAppxManifestProperties interface [App packaging and management],described, appxpackaging/IAppxManifestProperties, appxpkg.iappxmanifestproperties
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
 - IAppxManifestProperties
 - appxpackaging/IAppxManifestProperties
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
 - IAppxManifestProperties
---

# IAppxManifestProperties interface


## -description

Provides read-only access to the properties section of a package manifest.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAppxManifestProperties</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxManifestProperties</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAppxManifestProperties</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestproperties-getboolvalue">GetBoolValue</a>
</td>
<td align="left" width="63%">
Gets the value of the specified Boolean element in the properties section.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestproperties-getstringvalue">GetStringValue</a>
</td>
<td align="left" width="63%">
Gets the value of the specified string element in the properties section.

</td>
</tr>
</table>

## -remarks

The properties section of the manifest is defined using the <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-properties">Properties</a> element.

This object can be retrieved using the <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getproperties">IAppxManifestReader::GetProperties</a> method.


#### Examples

For an example, see <a href="/windows/desktop/appxpkg/how-to-query-package-identity-information">Quickstart: Read app package manifest info</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getproperties">IAppxManifestReader::GetProperties</a>