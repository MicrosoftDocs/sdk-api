---
UID: NN:appxpackaging.IAppxManifestPackageDependency
title: IAppxManifestPackageDependency (appxpackaging.h)
description: Describes the dependency of one package on another package. (IAppxManifestPackageDependency)
helpviewer_keywords: ["IAppxManifestPackageDependency","IAppxManifestPackageDependency interface [App packaging and management]","IAppxManifestPackageDependency interface [App packaging and management]","described","appxpackaging/IAppxManifestPackageDependency","appxpkg.iappxmanifestpackagedependency"]
old-location: appxpkg\iappxmanifestpackagedependency.htm
tech.root: appxpkg
ms.assetid: 1A5515DA-4A9E-40EE-9AAC-F267DAE9DDBA
ms.date: 12/05/2018
ms.keywords: IAppxManifestPackageDependency, IAppxManifestPackageDependency interface [App packaging and management], IAppxManifestPackageDependency interface [App packaging and management],described, appxpackaging/IAppxManifestPackageDependency, appxpkg.iappxmanifestpackagedependency
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
 - IAppxManifestPackageDependency
 - appxpackaging/IAppxManifestPackageDependency
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
 - IAppxManifestPackageDependency
---

# IAppxManifestPackageDependency interface


## -description

Describes the dependency of one package on another package.

## -inheritance

The <b>IAppxManifestPackageDependency</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAppxManifestPackageDependency</b> also has these types of members:

## -remarks

A dependency package is a package that the current package depends on, as specified in the package manifest using the <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-packagedependency">PackageDependency</a> element.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestpackagedependenciesenumerator">IAppxManifestPackageDependenciesEnumerator</a>
