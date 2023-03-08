---
UID: NF:appxpackaging.IAppxManifestPackageDependency.GetPublisher
title: IAppxManifestPackageDependency::GetPublisher (appxpackaging.h)
description: Gets the name of the publisher that produced the package on which the current package depends.
helpviewer_keywords: ["GetPublisher","GetPublisher method [App packaging and management]","GetPublisher method [App packaging and management]","IAppxManifestPackageDependency interface","IAppxManifestPackageDependency interface [App packaging and management]","GetPublisher method","IAppxManifestPackageDependency.GetPublisher","IAppxManifestPackageDependency::GetPublisher","appxpackaging/IAppxManifestPackageDependency::GetPublisher","appxpkg.iappxmanifestpackagedependency_getpublisher"]
old-location: appxpkg\iappxmanifestpackagedependency_getpublisher.htm
tech.root: appxpkg
ms.assetid: 0E307900-EA2F-44A4-A379-3192A234E399
ms.date: 12/05/2018
ms.keywords: GetPublisher, GetPublisher method [App packaging and management], GetPublisher method [App packaging and management],IAppxManifestPackageDependency interface, IAppxManifestPackageDependency interface [App packaging and management],GetPublisher method, IAppxManifestPackageDependency.GetPublisher, IAppxManifestPackageDependency::GetPublisher, appxpackaging/IAppxManifestPackageDependency::GetPublisher, appxpkg.iappxmanifestpackagedependency_getpublisher
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
 - IAppxManifestPackageDependency::GetPublisher
 - appxpackaging/IAppxManifestPackageDependency::GetPublisher
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
 - IAppxManifestPackageDependency.GetPublisher
---

# IAppxManifestPackageDependency::GetPublisher


## -description

Gets the name of the publisher that produced the package on which the current package depends.

## -parameters

### -param publisher [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a>*</b>

The name of the publisher.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the publisher is not defined for the dependency, this method returns <b>S_OK</b>, and <i>publisher</i> is <b>NULL</b>.

The caller must free the memory allocated for <i>publisher</i> using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestpackagedependency">IAppxManifestPackageDependency</a>