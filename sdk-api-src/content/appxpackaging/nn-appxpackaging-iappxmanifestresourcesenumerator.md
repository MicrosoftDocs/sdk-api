---
UID: NN:appxpackaging.IAppxManifestResourcesEnumerator
title: IAppxManifestResourcesEnumerator (appxpackaging.h)
description: Enumerates the resources defined in the package manifest.
helpviewer_keywords: ["IAppxManifestResourcesEnumerator","IAppxManifestResourcesEnumerator interface [App packaging and management]","IAppxManifestResourcesEnumerator interface [App packaging and management]","described","appxpackaging/IAppxManifestResourcesEnumerator","appxpkg.iappxmanifestresourcesenumerator"]
old-location: appxpkg\iappxmanifestresourcesenumerator.htm
tech.root: appxpkg
ms.assetid: D76C7512-962F-4AFE-934F-BBC215B5FE99
ms.date: 12/05/2018
ms.keywords: IAppxManifestResourcesEnumerator, IAppxManifestResourcesEnumerator interface [App packaging and management], IAppxManifestResourcesEnumerator interface [App packaging and management],described, appxpackaging/IAppxManifestResourcesEnumerator, appxpkg.iappxmanifestresourcesenumerator
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
 - IAppxManifestResourcesEnumerator
 - appxpackaging/IAppxManifestResourcesEnumerator
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
 - IAppxManifestResourcesEnumerator
---

# IAppxManifestResourcesEnumerator interface


## -description

Enumerates the resources defined in the package manifest.

## -inheritance

The <b>IAppxManifestResourcesEnumerator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxManifestResourcesEnumerator</b> also has these types of members:

## -remarks

This object can be retrieved by using the <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getresources">GetResources</a> method of a  <a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader">IAppxManifestReader</a> or <a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader2">IAppxManifestReader2</a> object. But, starting with Windows 8.1, use <b>IAppxManifestReader2::GetResources</b> because it iterates over more resource qualifiers, such as, <b>Scale</b> and <b>DXFeatureLevel</b>.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader">IAppxManifestReader</a>



<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader2">IAppxManifestReader2</a>



<a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getresources">IAppxManifestReader::GetResources</a>
