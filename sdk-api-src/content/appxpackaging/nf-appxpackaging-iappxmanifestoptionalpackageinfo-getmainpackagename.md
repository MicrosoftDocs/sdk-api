---
UID: NF:appxpackaging.IAppxManifestOptionalPackageInfo.GetMainPackageName
title: IAppxManifestOptionalPackageInfo::GetMainPackageName (appxpackaging.h)
description: Gets the main package name from the optional package.
helpviewer_keywords: ["GetMainPackageName","GetMainPackageName method [App packaging and management]","GetMainPackageName method [App packaging and management]","IAppxManifestOptionalPackageInfo interface","IAppxManifestOptionalPackageInfo interface [App packaging and management]","GetMainPackageName method","IAppxManifestOptionalPackageInfo.GetMainPackageName","IAppxManifestOptionalPackageInfo::GetMainPackageName","appxpackaging/IAppxManifestOptionalPackageInfo::GetMainPackageName","appxpkg.iappxmanifestoptionalpackageinfo_getmainpackagename"]
old-location: appxpkg\iappxmanifestoptionalpackageinfo_getmainpackagename.htm
tech.root: appxpkg
ms.assetid: 95CD6739-06B2-4862-8313-4133AFBFD583
ms.date: 12/05/2018
ms.keywords: GetMainPackageName, GetMainPackageName method [App packaging and management], GetMainPackageName method [App packaging and management],IAppxManifestOptionalPackageInfo interface, IAppxManifestOptionalPackageInfo interface [App packaging and management],GetMainPackageName method, IAppxManifestOptionalPackageInfo.GetMainPackageName, IAppxManifestOptionalPackageInfo::GetMainPackageName, appxpackaging/IAppxManifestOptionalPackageInfo::GetMainPackageName, appxpkg.iappxmanifestoptionalpackageinfo_getmainpackagename
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
 - IAppxManifestOptionalPackageInfo::GetMainPackageName
 - appxpackaging/IAppxManifestOptionalPackageInfo::GetMainPackageName
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
 - IAppxManifestOptionalPackageInfo.GetMainPackageName
---

# IAppxManifestOptionalPackageInfo::GetMainPackageName


## -description

Gets the main package name from the optional package.

## -parameters

### -param mainPackageName [out, retval]

The main package name.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestoptionalpackageinfo">IAppxManifestOptionalPackageInfo</a>