---
UID: NF:appxpackaging.IAppxManifestOptionalPackageInfo.GetIsOptionalPackage
title: IAppxManifestOptionalPackageInfo::GetIsOptionalPackage (appxpackaging.h)
description: Determines whether the package is optional.
helpviewer_keywords: ["GetIsOptionalPackage","GetIsOptionalPackage method [App packaging and management]","GetIsOptionalPackage method [App packaging and management]","IAppxManifestOptionalPackageInfo interface","IAppxManifestOptionalPackageInfo interface [App packaging and management]","GetIsOptionalPackage method","IAppxManifestOptionalPackageInfo.GetIsOptionalPackage","IAppxManifestOptionalPackageInfo::GetIsOptionalPackage","appxpackaging/IAppxManifestOptionalPackageInfo::GetIsOptionalPackage","appxpkg.iappxmanifestoptionalpackageinfo_getisoptionalpackage"]
old-location: appxpkg\iappxmanifestoptionalpackageinfo_getisoptionalpackage.htm
tech.root: appxpkg
ms.assetid: E52E411C-0A3E-4DA3-B25D-14E761FEF676
ms.date: 12/05/2018
ms.keywords: GetIsOptionalPackage, GetIsOptionalPackage method [App packaging and management], GetIsOptionalPackage method [App packaging and management],IAppxManifestOptionalPackageInfo interface, IAppxManifestOptionalPackageInfo interface [App packaging and management],GetIsOptionalPackage method, IAppxManifestOptionalPackageInfo.GetIsOptionalPackage, IAppxManifestOptionalPackageInfo::GetIsOptionalPackage, appxpackaging/IAppxManifestOptionalPackageInfo::GetIsOptionalPackage, appxpkg.iappxmanifestoptionalpackageinfo_getisoptionalpackage
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
 - IAppxManifestOptionalPackageInfo::GetIsOptionalPackage
 - appxpackaging/IAppxManifestOptionalPackageInfo::GetIsOptionalPackage
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
 - IAppxManifestOptionalPackageInfo.GetIsOptionalPackage
---

# IAppxManifestOptionalPackageInfo::GetIsOptionalPackage


## -description

Determines whether the package is optional.

## -parameters

### -param isOptionalPackage [out, retval]

True if the package is optional, false otherwise.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestoptionalpackageinfo">IAppxManifestOptionalPackageInfo</a>