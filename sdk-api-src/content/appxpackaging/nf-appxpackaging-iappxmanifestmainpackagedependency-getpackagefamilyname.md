---
UID: NF:appxpackaging.IAppxManifestMainPackageDependency.GetPackageFamilyName
title: IAppxManifestMainPackageDependency::GetPackageFamilyName (appxpackaging.h)
description: Gets the package family name of the main package dependency from the AppxManifest.xml.
helpviewer_keywords: ["GetPackageFamilyName","GetPackageFamilyName method [App packaging and management]","GetPackageFamilyName method [App packaging and management]","IAppxManifestMainPackageDependency interface","IAppxManifestMainPackageDependency interface [App packaging and management]","GetPackageFamilyName method","IAppxManifestMainPackageDependency.GetPackageFamilyName","IAppxManifestMainPackageDependency::GetPackageFamilyName","appxpackaging/IAppxManifestMainPackageDependency::GetPackageFamilyName","appxpkg.iappxmanifestmainpackagedependency_getpackagefamilyname"]
old-location: appxpkg\iappxmanifestmainpackagedependency_getpackagefamilyname.htm
tech.root: appxpkg
ms.assetid: 4F8E3E60-CE14-48C1-8367-10AA293F72F6
ms.date: 12/05/2018
ms.keywords: GetPackageFamilyName, GetPackageFamilyName method [App packaging and management], GetPackageFamilyName method [App packaging and management],IAppxManifestMainPackageDependency interface, IAppxManifestMainPackageDependency interface [App packaging and management],GetPackageFamilyName method, IAppxManifestMainPackageDependency.GetPackageFamilyName, IAppxManifestMainPackageDependency::GetPackageFamilyName, appxpackaging/IAppxManifestMainPackageDependency::GetPackageFamilyName, appxpkg.iappxmanifestmainpackagedependency_getpackagefamilyname
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
 - IAppxManifestMainPackageDependency::GetPackageFamilyName
 - appxpackaging/IAppxManifestMainPackageDependency::GetPackageFamilyName
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
 - IAppxManifestMainPackageDependency.GetPackageFamilyName
---

# IAppxManifestMainPackageDependency::GetPackageFamilyName


## -description

Gets the package family name of the main package dependency from the AppxManifest.xml.

## -parameters

### -param packageFamilyName [out, retval]

The package family name of the main package dependency.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestmainpackagedependency">IAppxManifestMainPackageDependency</a>