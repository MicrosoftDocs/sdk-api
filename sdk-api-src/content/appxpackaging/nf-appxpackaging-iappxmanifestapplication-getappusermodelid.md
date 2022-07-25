---
UID: NF:appxpackaging.IAppxManifestApplication.GetAppUserModelId
title: IAppxManifestApplication::GetAppUserModelId (appxpackaging.h)
description: Gets the application user model identifier.
helpviewer_keywords: ["GetAppUserModelId","GetAppUserModelId method [App packaging and management]","GetAppUserModelId method [App packaging and management]","IAppxManifestApplication interface","IAppxManifestApplication interface [App packaging and management]","GetAppUserModelId method","IAppxManifestApplication.GetAppUserModelId","IAppxManifestApplication::GetAppUserModelId","appxpackaging/IAppxManifestApplication::GetAppUserModelId","appxpkg.iappxmanifestapplication_getappusermodelid"]
old-location: appxpkg\iappxmanifestapplication_getappusermodelid.htm
tech.root: appxpkg
ms.assetid: A1CD62B4-A314-43B3-AD80-3EB3EDF63B3D
ms.date: 12/05/2018
ms.keywords: GetAppUserModelId, GetAppUserModelId method [App packaging and management], GetAppUserModelId method [App packaging and management],IAppxManifestApplication interface, IAppxManifestApplication interface [App packaging and management],GetAppUserModelId method, IAppxManifestApplication.GetAppUserModelId, IAppxManifestApplication::GetAppUserModelId, appxpackaging/IAppxManifestApplication::GetAppUserModelId, appxpkg.iappxmanifestapplication_getappusermodelid
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
 - IAppxManifestApplication::GetAppUserModelId
 - appxpackaging/IAppxManifestApplication::GetAppUserModelId
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
 - IAppxManifestApplication.GetAppUserModelId
---

# IAppxManifestApplication::GetAppUserModelId


## -description

Gets the application user model identifier.

## -parameters

### -param appUserModelId [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a>*</b>

The user model identifier.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The caller must free the memory allocated for <i>appUserModelId</i> using the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function.

## -see-also

<a href="/windows/desktop/shell/appids">Application User Model IDs</a>



<b>Concepts</b>



<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestapplication">IAppxManifestApplication</a>



<b>Reference</b>