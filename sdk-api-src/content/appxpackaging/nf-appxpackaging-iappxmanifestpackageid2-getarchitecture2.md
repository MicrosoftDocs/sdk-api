---
UID: NF:appxpackaging.IAppxManifestPackageId2.GetArchitecture2
title: IAppxManifestPackageId2::GetArchitecture2 (appxpackaging.h)
description: Gets the processor architecture as defined in the manifest. (IAppxManifestPackageId2.GetArchitecture2)
helpviewer_keywords: ["GetArchitecture2","GetArchitecture2 method [App packaging and management]","GetArchitecture2 method [App packaging and management]","IAppxManifestPackageId2 interface","IAppxManifestPackageId2 interface [App packaging and management]","GetArchitecture2 method","IAppxManifestPackageId2.GetArchitecture2","IAppxManifestPackageId2::GetArchitecture2","appxpackaging/IAppxManifestPackageId2::GetArchitecture2","appxpkg.iappxmanifestpackageid2_getarchitecture2"]
old-location: appxpkg\iappxmanifestpackageid2_getarchitecture2.htm
tech.root: appxpkg
ms.assetid: FBC34FBA-C6BB-45AD-8005-5C2B91A1369D
ms.date: 12/05/2018
ms.keywords: GetArchitecture2, GetArchitecture2 method [App packaging and management], GetArchitecture2 method [App packaging and management],IAppxManifestPackageId2 interface, IAppxManifestPackageId2 interface [App packaging and management],GetArchitecture2 method, IAppxManifestPackageId2.GetArchitecture2, IAppxManifestPackageId2::GetArchitecture2, appxpackaging/IAppxManifestPackageId2::GetArchitecture2, appxpkg.iappxmanifestpackageid2_getarchitecture2
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
 - IAppxManifestPackageId2::GetArchitecture2
 - appxpackaging/IAppxManifestPackageId2::GetArchitecture2
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
 - IAppxManifestPackageId2.GetArchitecture2
---

# IAppxManifestPackageId2::GetArchitecture2


## -description

Gets the processor architecture as defined in the manifest.

## -parameters

### -param architecture [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/ne-appxpackaging-appx_package_architecture2">APPX_PACKAGE_ARCHITECTURE2</a>*</b>

The architecture specified for the package.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Processor architecture information is specified using the <b>ProcessorArchitecture</b> attribute of the <b>Identity</b> element in the app package manifest.

If no architecture is defined in the manifest, this method returns the <b>APPX_PACKAGE_ARCHITECTURE_NEUTRAL</b> value of the  <a href="/windows/desktop/api/appxpackaging/ne-appxpackaging-appx_package_architecture2">APPX_PACKAGE_ARCHITECTURE2</a> enumeration.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestpackageid2">IAppxManifestPackageId2</a>
