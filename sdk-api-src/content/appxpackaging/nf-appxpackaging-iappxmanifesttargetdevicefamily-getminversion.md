---
UID: NF:appxpackaging.IAppxManifestTargetDeviceFamily.GetMinVersion
title: IAppxManifestTargetDeviceFamily::GetMinVersion (appxpackaging.h)
description: Gets the minimum version of the target device family from the AppxManifest.xml.
helpviewer_keywords: ["GetMinVersion","GetMinVersion method [App packaging and management]","GetMinVersion method [App packaging and management]","IAppxManifestTargetDeviceFamily interface","IAppxManifestTargetDeviceFamily interface [App packaging and management]","GetMinVersion method","IAppxManifestTargetDeviceFamily.GetMinVersion","IAppxManifestTargetDeviceFamily::GetMinVersion","appxpackaging/IAppxManifestTargetDeviceFamily::GetMinVersion","appxpkg.iappxmanifesttargetdevicefamily_getminversion"]
old-location: appxpkg\iappxmanifesttargetdevicefamily_getminversion.htm
tech.root: appxpkg
ms.assetid: 8CE408D3-0DD7-4482-8F7E-FE731ACE58C6
ms.date: 12/05/2018
ms.keywords: GetMinVersion, GetMinVersion method [App packaging and management], GetMinVersion method [App packaging and management],IAppxManifestTargetDeviceFamily interface, IAppxManifestTargetDeviceFamily interface [App packaging and management],GetMinVersion method, IAppxManifestTargetDeviceFamily.GetMinVersion, IAppxManifestTargetDeviceFamily::GetMinVersion, appxpackaging/IAppxManifestTargetDeviceFamily::GetMinVersion, appxpkg.iappxmanifesttargetdevicefamily_getminversion
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
 - IAppxManifestTargetDeviceFamily::GetMinVersion
 - appxpackaging/IAppxManifestTargetDeviceFamily::GetMinVersion
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
 - IAppxManifestTargetDeviceFamily.GetMinVersion
---

# IAppxManifestTargetDeviceFamily::GetMinVersion


## -description

Gets the minimum version of the target device family from the AppxManifest.xml.

## -parameters

### -param minVersion [out, retval]

The minimum version.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifesttargetdevicefamily">IAppxManifestTargetDeviceFamily</a>