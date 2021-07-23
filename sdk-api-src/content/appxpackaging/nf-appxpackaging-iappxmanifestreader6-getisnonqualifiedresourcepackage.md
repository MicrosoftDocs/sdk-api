---
UID: NF:appxpackaging.IAppxManifestReader6.GetIsNonQualifiedResourcePackage
title: IAppxManifestReader6::GetIsNonQualifiedResourcePackage (appxpackaging.h)
description: Queries whether an app package is a non-qualified resource package.
helpviewer_keywords: ["GetIsNonQualifiedResourcePackage","GetIsNonQualifiedResourcePackage method [App packaging and management]","GetIsNonQualifiedResourcePackage method [App packaging and management]","IAppxManifestReader6 interface","IAppxManifestReader6 interface [App packaging and management]","GetIsNonQualifiedResourcePackage method","IAppxManifestReader6.GetIsNonQualifiedResourcePackage","IAppxManifestReader6::GetIsNonQualifiedResourcePackage","appxpackaging/IAppxManifestReader6::GetIsNonQualifiedResourcePackage","appxpkg.iappxmanifestreader6_getisnonqualifiedresourcepackage"]
old-location: appxpkg\iappxmanifestreader6_getisnonqualifiedresourcepackage.htm
tech.root: appxpkg
ms.assetid: E6E8D383-E9E9-4615-B220-B0666E6C2CA2
ms.date: 12/05/2018
ms.keywords: GetIsNonQualifiedResourcePackage, GetIsNonQualifiedResourcePackage method [App packaging and management], GetIsNonQualifiedResourcePackage method [App packaging and management],IAppxManifestReader6 interface, IAppxManifestReader6 interface [App packaging and management],GetIsNonQualifiedResourcePackage method, IAppxManifestReader6.GetIsNonQualifiedResourcePackage, IAppxManifestReader6::GetIsNonQualifiedResourcePackage, appxpackaging/IAppxManifestReader6::GetIsNonQualifiedResourcePackage, appxpkg.iappxmanifestreader6_getisnonqualifiedresourcepackage
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
 - IAppxManifestReader6::GetIsNonQualifiedResourcePackage
 - appxpackaging/IAppxManifestReader6::GetIsNonQualifiedResourcePackage
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
 - IAppxManifestReader6.GetIsNonQualifiedResourcePackage
---

# IAppxManifestReader6::GetIsNonQualifiedResourcePackage


## -description

Queries whether an app package is a non-qualified resource package.

## -parameters

### -param isNonQualifiedResourcePackage [out, retval]

True if the package is a non-qualified resource package, False otherwise.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader6">IAppxManifestReader6</a>