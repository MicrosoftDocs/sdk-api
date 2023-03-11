---
UID: NF:appxpackaging.IAppxManifestPackageId.GetArchitecture
title: IAppxManifestPackageId::GetArchitecture (appxpackaging.h)
description: Gets the processor architecture as defined in the manifest. (IAppxManifestPackageId.GetArchitecture)
helpviewer_keywords: ["GetArchitecture","GetArchitecture method [App packaging and management]","GetArchitecture method [App packaging and management]","IAppxManifestPackageId interface","IAppxManifestPackageId interface [App packaging and management]","GetArchitecture method","IAppxManifestPackageId.GetArchitecture","IAppxManifestPackageId::GetArchitecture","appxpackaging/IAppxManifestPackageId::GetArchitecture","appxpkg.iappxmanifestpackageid_getarchitecture"]
old-location: appxpkg\iappxmanifestpackageid_getarchitecture.htm
tech.root: appxpkg
ms.assetid: 0A332C96-9535-4BD3-B4D2-39559E430870
ms.date: 12/05/2018
ms.keywords: GetArchitecture, GetArchitecture method [App packaging and management], GetArchitecture method [App packaging and management],IAppxManifestPackageId interface, IAppxManifestPackageId interface [App packaging and management],GetArchitecture method, IAppxManifestPackageId.GetArchitecture, IAppxManifestPackageId::GetArchitecture, appxpackaging/IAppxManifestPackageId::GetArchitecture, appxpkg.iappxmanifestpackageid_getarchitecture
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
 - IAppxManifestPackageId::GetArchitecture
 - appxpackaging/IAppxManifestPackageId::GetArchitecture
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
 - IAppxManifestPackageId.GetArchitecture
---

# IAppxManifestPackageId::GetArchitecture


## -description

Gets the processor architecture as defined in the manifest.

## -parameters

### -param architecture [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/ne-appxpackaging-appx_package_architecture">APPX_PACKAGE_ARCHITECTURE</a>*</b>

The architecture specified for the package.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Processor architecture information is specified using the <b>ProcessorArchitecture</b> attribute of the <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity">Identity</a> element in the package manifest.

If no architecture is defined in the manifest, this method returns the <b>APPX_PACKAGE_ARCHITECTURE_NEUTRAL</b> value of the  <a href="/windows/desktop/api/appxpackaging/ne-appxpackaging-appx_package_architecture">APPX_PACKAGE_ARCHITECTURE</a> enumeration.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestpackageid">IAppxManifestPackageId</a>
