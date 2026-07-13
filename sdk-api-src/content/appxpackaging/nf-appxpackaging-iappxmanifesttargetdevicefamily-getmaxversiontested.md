---
UID: NF:appxpackaging.IAppxManifestTargetDeviceFamily.GetMaxVersionTested
title: IAppxManifestTargetDeviceFamily::GetMaxVersionTested (appxpackaging.h)
description: Gets the maximum version tested from the AppxManifest.xml.
helpviewer_keywords: ["GetMaxVersionTested","GetMaxVersionTested method [App packaging and management]","GetMaxVersionTested method [App packaging and management]","IAppxManifestTargetDeviceFamily interface","IAppxManifestTargetDeviceFamily interface [App packaging and management]","GetMaxVersionTested method","IAppxManifestTargetDeviceFamily.GetMaxVersionTested","IAppxManifestTargetDeviceFamily::GetMaxVersionTested","appxpackaging/IAppxManifestTargetDeviceFamily::GetMaxVersionTested","appxpkg.iappxmanifesttargetdevicefamily_getmaxversiontested"]
old-location: appxpkg\iappxmanifesttargetdevicefamily_getmaxversiontested.htm
tech.root: appxpkg
ms.assetid: 65391D03-627D-4302-BE1A-6E90E3A04458
ms.date: 12/05/2018
ms.keywords: GetMaxVersionTested, GetMaxVersionTested method [App packaging and management], GetMaxVersionTested method [App packaging and management],IAppxManifestTargetDeviceFamily interface, IAppxManifestTargetDeviceFamily interface [App packaging and management],GetMaxVersionTested method, IAppxManifestTargetDeviceFamily.GetMaxVersionTested, IAppxManifestTargetDeviceFamily::GetMaxVersionTested, appxpackaging/IAppxManifestTargetDeviceFamily::GetMaxVersionTested, appxpkg.iappxmanifesttargetdevicefamily_getmaxversiontested
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
 - IAppxManifestTargetDeviceFamily::GetMaxVersionTested
 - appxpackaging/IAppxManifestTargetDeviceFamily::GetMaxVersionTested
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
 - IAppxManifestTargetDeviceFamily.GetMaxVersionTested
---

# IAppxManifestTargetDeviceFamily::GetMaxVersionTested


## -description

Gets the maximum version tested from the AppxManifest.xml.

## -parameters

### -param maxVersionTested [out, retval]

The max version tested attribute.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifesttargetdevicefamily">IAppxManifestTargetDeviceFamily</a>