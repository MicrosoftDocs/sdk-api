---
UID: NF:appxpackaging.IAppxManifestMainPackageDependency.GetName
title: IAppxManifestMainPackageDependency::GetName (appxpackaging.h)
description: Gets the name of the main package dependency from the AppxManifest.xml.
helpviewer_keywords: ["GetName","GetName method [App packaging and management]","GetName method [App packaging and management]","IAppxManifestMainPackageDependency interface","IAppxManifestMainPackageDependency interface [App packaging and management]","GetName method","IAppxManifestMainPackageDependency.GetName","IAppxManifestMainPackageDependency::GetName","appxpackaging/IAppxManifestMainPackageDependency::GetName","appxpkg.iappxmanifestmainpackagedependency_getname"]
old-location: appxpkg\iappxmanifestmainpackagedependency_getname.htm
tech.root: appxpkg
ms.assetid: 0D891C01-F149-4BF0-99E7-E2AAD6D781AD
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [App packaging and management], GetName method [App packaging and management],IAppxManifestMainPackageDependency interface, IAppxManifestMainPackageDependency interface [App packaging and management],GetName method, IAppxManifestMainPackageDependency.GetName, IAppxManifestMainPackageDependency::GetName, appxpackaging/IAppxManifestMainPackageDependency::GetName, appxpkg.iappxmanifestmainpackagedependency_getname
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
 - IAppxManifestMainPackageDependency::GetName
 - appxpackaging/IAppxManifestMainPackageDependency::GetName
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
 - IAppxManifestMainPackageDependency.GetName
---

# IAppxManifestMainPackageDependency::GetName


## -description

Gets the name of the main package dependency from the AppxManifest.xml.

## -parameters

### -param name [out, retval]

The name of the main package dependency.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestmainpackagedependency">IAppxManifestMainPackageDependency</a>