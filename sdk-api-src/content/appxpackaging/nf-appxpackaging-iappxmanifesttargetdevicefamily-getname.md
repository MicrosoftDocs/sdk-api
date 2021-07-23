---
UID: NF:appxpackaging.IAppxManifestTargetDeviceFamily.GetName
title: IAppxManifestTargetDeviceFamily::GetName (appxpackaging.h)
description: Gets the name of the target device family from the AppxManifest.xml..
helpviewer_keywords: ["GetName","GetName method [App packaging and management]","GetName method [App packaging and management]","IAppxManifestTargetDeviceFamily interface","IAppxManifestTargetDeviceFamily interface [App packaging and management]","GetName method","IAppxManifestTargetDeviceFamily.GetName","IAppxManifestTargetDeviceFamily::GetName","appxpackaging/IAppxManifestTargetDeviceFamily::GetName","appxpkg.iappxmanifesttargetdevicefamily_getname"]
old-location: appxpkg\iappxmanifesttargetdevicefamily_getname.htm
tech.root: appxpkg
ms.assetid: B7D3A0D3-421D-4A40-AF40-516AE51E06D4
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [App packaging and management], GetName method [App packaging and management],IAppxManifestTargetDeviceFamily interface, IAppxManifestTargetDeviceFamily interface [App packaging and management],GetName method, IAppxManifestTargetDeviceFamily.GetName, IAppxManifestTargetDeviceFamily::GetName, appxpackaging/IAppxManifestTargetDeviceFamily::GetName, appxpkg.iappxmanifesttargetdevicefamily_getname
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
 - IAppxManifestTargetDeviceFamily::GetName
 - appxpackaging/IAppxManifestTargetDeviceFamily::GetName
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
 - IAppxManifestTargetDeviceFamily.GetName
---

# IAppxManifestTargetDeviceFamily::GetName


## -description

Gets the name of the target device family from the AppxManifest.xml..

## -parameters

### -param name [out, retval]

The target device family name.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifesttargetdevicefamily">IAppxManifestTargetDeviceFamily</a>