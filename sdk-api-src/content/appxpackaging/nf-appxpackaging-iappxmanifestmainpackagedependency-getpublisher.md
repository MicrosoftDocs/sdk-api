---
UID: NF:appxpackaging.IAppxManifestMainPackageDependency.GetPublisher
title: IAppxManifestMainPackageDependency::GetPublisher (appxpackaging.h)
description: Gets the publisher of the main package dependency from the AppxManifest.xml.
helpviewer_keywords: ["GetPublisher","GetPublisher method [App packaging and management]","GetPublisher method [App packaging and management]","IAppxManifestMainPackageDependency interface","IAppxManifestMainPackageDependency interface [App packaging and management]","GetPublisher method","IAppxManifestMainPackageDependency.GetPublisher","IAppxManifestMainPackageDependency::GetPublisher","appxpackaging/IAppxManifestMainPackageDependency::GetPublisher","appxpkg.iappxmanifestmainpackagedependency_getpublisher"]
old-location: appxpkg\iappxmanifestmainpackagedependency_getpublisher.htm
tech.root: appxpkg
ms.assetid: 4E7AD93A-27B6-4FE0-8803-EF1ACCB82986
ms.date: 12/05/2018
ms.keywords: GetPublisher, GetPublisher method [App packaging and management], GetPublisher method [App packaging and management],IAppxManifestMainPackageDependency interface, IAppxManifestMainPackageDependency interface [App packaging and management],GetPublisher method, IAppxManifestMainPackageDependency.GetPublisher, IAppxManifestMainPackageDependency::GetPublisher, appxpackaging/IAppxManifestMainPackageDependency::GetPublisher, appxpkg.iappxmanifestmainpackagedependency_getpublisher
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
 - IAppxManifestMainPackageDependency::GetPublisher
 - appxpackaging/IAppxManifestMainPackageDependency::GetPublisher
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
 - IAppxManifestMainPackageDependency.GetPublisher
---

# IAppxManifestMainPackageDependency::GetPublisher


## -description

Gets the publisher of the main package dependency from the AppxManifest.xml.

## -parameters

### -param publisher [out, retval]

The publisher of the main package dependency.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestmainpackagedependency">IAppxManifestMainPackageDependency</a>