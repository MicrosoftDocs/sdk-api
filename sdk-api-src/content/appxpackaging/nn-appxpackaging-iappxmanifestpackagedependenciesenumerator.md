---
UID: NN:appxpackaging.IAppxManifestPackageDependenciesEnumerator
title: IAppxManifestPackageDependenciesEnumerator (appxpackaging.h)
description: Enumerates the package dependencies defined in the package manifest.
helpviewer_keywords: ["IAppxManifestPackageDependenciesEnumerator","IAppxManifestPackageDependenciesEnumerator interface [App packaging and management]","IAppxManifestPackageDependenciesEnumerator interface [App packaging and management]","described","appxpackaging/IAppxManifestPackageDependenciesEnumerator","appxpkg.iappxmanifestpackagedependenciesenumerator"]
old-location: appxpkg\iappxmanifestpackagedependenciesenumerator.htm
tech.root: appxpkg
ms.assetid: A09709AE-301F-4457-8E02-1A88FB283A43
ms.date: 12/05/2018
ms.keywords: IAppxManifestPackageDependenciesEnumerator, IAppxManifestPackageDependenciesEnumerator interface [App packaging and management], IAppxManifestPackageDependenciesEnumerator interface [App packaging and management],described, appxpackaging/IAppxManifestPackageDependenciesEnumerator, appxpkg.iappxmanifestpackagedependenciesenumerator
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
 - IAppxManifestPackageDependenciesEnumerator
 - appxpackaging/IAppxManifestPackageDependenciesEnumerator
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
 - IAppxManifestPackageDependenciesEnumerator
---

# IAppxManifestPackageDependenciesEnumerator interface


## -description

Enumerates  the package dependencies defined in the package manifest.

## -inheritance

The <b>IAppxManifestPackageDependenciesEnumerator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxManifestPackageDependenciesEnumerator</b> also has these types of members:

## -remarks

This object can be retrieved using the <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestreader-getpackagedependencies">IAppxManifestReader::GetPackageDependencies</a> method.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestpackagedependency">IAppxManifestPackageDependency</a>
