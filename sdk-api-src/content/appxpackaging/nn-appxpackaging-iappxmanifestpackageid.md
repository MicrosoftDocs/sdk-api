---
UID: NN:appxpackaging.IAppxManifestPackageId
title: IAppxManifestPackageId (appxpackaging.h)
description: Provides access to the package identity.
helpviewer_keywords: ["IAppxManifestPackageId","IAppxManifestPackageId interface [App packaging and management]","IAppxManifestPackageId interface [App packaging and management]","described","appxpackaging/IAppxManifestPackageId","appxpkg.iappxmanifestpackageid"]
old-location: appxpkg\iappxmanifestpackageid.htm
tech.root: appxpkg
ms.assetid: 8665AC2B-4D06-4684-99B1-E22533CA04AA
ms.date: 12/05/2018
ms.keywords: IAppxManifestPackageId, IAppxManifestPackageId interface [App packaging and management], IAppxManifestPackageId interface [App packaging and management],described, appxpackaging/IAppxManifestPackageId, appxpkg.iappxmanifestpackageid
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
 - IAppxManifestPackageId
 - appxpackaging/IAppxManifestPackageId
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
 - IAppxManifestPackageId
---

# IAppxManifestPackageId interface


## -description

Provides access to the package identity.

## -inheritance

The <b>IAppxManifestPackageId</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxManifestPackageId</b> also has these types of members:

## -remarks

Package identity information is specified using the <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity">Identity</a> element in the package manifest.

This object can be retrieved using the <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getpackageid">IAppxManifestReader::GetPackageId</a> method.


#### Examples

For an example, see <a href="/windows/desktop/appxpkg/how-to-query-package-identity-information">Quickstart: Read app package manifest info</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader">IAppxManifestReader</a>



<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getpackageid">IAppxManifestReader::GetPackageId</a>
