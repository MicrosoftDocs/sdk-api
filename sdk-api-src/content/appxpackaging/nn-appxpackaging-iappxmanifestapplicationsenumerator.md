---
UID: NN:appxpackaging.IAppxManifestApplicationsEnumerator
title: IAppxManifestApplicationsEnumerator (appxpackaging.h)
description: Enumerates the applications defined in the package manifest.
helpviewer_keywords: ["IAppxManifestApplicationsEnumerator","IAppxManifestApplicationsEnumerator interface [App packaging and management]","IAppxManifestApplicationsEnumerator interface [App packaging and management]","described","appxpackaging/IAppxManifestApplicationsEnumerator","appxpkg.iappxmanifestapplicationsenumerator"]
old-location: appxpkg\iappxmanifestapplicationsenumerator.htm
tech.root: appxpkg
ms.assetid: 49955DE0-A6BE-4FD7-B8E3-E4126B3C4B8F
ms.date: 12/05/2018
ms.keywords: IAppxManifestApplicationsEnumerator, IAppxManifestApplicationsEnumerator interface [App packaging and management], IAppxManifestApplicationsEnumerator interface [App packaging and management],described, appxpackaging/IAppxManifestApplicationsEnumerator, appxpkg.iappxmanifestapplicationsenumerator
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
 - IAppxManifestApplicationsEnumerator
 - appxpackaging/IAppxManifestApplicationsEnumerator
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
 - IAppxManifestApplicationsEnumerator
---

# IAppxManifestApplicationsEnumerator interface


## -description

Enumerates the applications defined in the package manifest.

## -inheritance

The <b>IAppxManifestApplicationsEnumerator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxManifestApplicationsEnumerator</b> also has these types of members:

## -remarks

Applications are specified using the <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-applications">Applications</a> element in the package manifest.

This object can be retrieved using the <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getapplications">IAppxManifestReader::GetApplications</a> method.


#### Examples

For an example, see <a href="/windows/desktop/appxpkg/how-to-query-package-identity-information">Quickstart: Read app package manifest info</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestapplication">IAppxManifestApplication</a>



<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getapplications">IAppxManifestReader::GetApplications</a>
