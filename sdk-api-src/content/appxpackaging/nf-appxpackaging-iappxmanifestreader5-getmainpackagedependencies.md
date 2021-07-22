---
UID: NF:appxpackaging.IAppxManifestReader5.GetMainPackageDependencies
title: IAppxManifestReader5::GetMainPackageDependencies (appxpackaging.h)
description: Gets a main package dependencies enumerator.
helpviewer_keywords: ["GetMainPackageDependencies","GetMainPackageDependencies method [App packaging and management]","GetMainPackageDependencies method [App packaging and management]","IAppxManifestReader5 interface","IAppxManifestReader5 interface [App packaging and management]","GetMainPackageDependencies method","IAppxManifestReader5.GetMainPackageDependencies","IAppxManifestReader5::GetMainPackageDependencies","appxpackaging/IAppxManifestReader5::GetMainPackageDependencies","appxpkg.iappxmanifestreader5_getmainpackagedependencies"]
old-location: appxpkg\iappxmanifestreader5_getmainpackagedependencies.htm
tech.root: appxpkg
ms.assetid: E89A6A43-28F6-4A9A-A8B7-3450B68E3DB1
ms.date: 12/05/2018
ms.keywords: GetMainPackageDependencies, GetMainPackageDependencies method [App packaging and management], GetMainPackageDependencies method [App packaging and management],IAppxManifestReader5 interface, IAppxManifestReader5 interface [App packaging and management],GetMainPackageDependencies method, IAppxManifestReader5.GetMainPackageDependencies, IAppxManifestReader5::GetMainPackageDependencies, appxpackaging/IAppxManifestReader5::GetMainPackageDependencies, appxpkg.iappxmanifestreader5_getmainpackagedependencies
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
 - IAppxManifestReader5::GetMainPackageDependencies
 - appxpackaging/IAppxManifestReader5::GetMainPackageDependencies
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
 - IAppxManifestReader5.GetMainPackageDependencies
---

# IAppxManifestReader5::GetMainPackageDependencies


## -description

Gets a main package dependencies enumerator.

## -parameters

### -param mainPackageDependencies [out, retval]

The main package dependencies enumerator.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestreader5">IAppxManifestReader5</a>