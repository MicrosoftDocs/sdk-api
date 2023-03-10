---
UID: NF:appxpackaging.IAppxBundleManifestOptionalBundleInfo.GetFileName
title: IAppxBundleManifestOptionalBundleInfo::GetFileName (appxpackaging.h)
description: Retrieves the file-name attribute of the &lt;OptionalBundle&gt;.
helpviewer_keywords: ["GetFileName","GetFileName method [App packaging and management]","GetFileName method [App packaging and management]","IAppxBundleManifestOptionalBundleInfo interface","IAppxBundleManifestOptionalBundleInfo interface [App packaging and management]","GetFileName method","IAppxBundleManifestOptionalBundleInfo.GetFileName","IAppxBundleManifestOptionalBundleInfo::GetFileName","appxpackaging/IAppxBundleManifestOptionalBundleInfo::GetFileName","appxpkg.iappxbundlemanifestoptionalbundleinfo_getfilename"]
old-location: appxpkg\iappxbundlemanifestoptionalbundleinfo_getfilename.htm
tech.root: appxpkg
ms.assetid: 6553DAC3-D938-4653-8DE4-A5CA02640D31
ms.date: 12/05/2018
ms.keywords: GetFileName, GetFileName method [App packaging and management], GetFileName method [App packaging and management],IAppxBundleManifestOptionalBundleInfo interface, IAppxBundleManifestOptionalBundleInfo interface [App packaging and management],GetFileName method, IAppxBundleManifestOptionalBundleInfo.GetFileName, IAppxBundleManifestOptionalBundleInfo::GetFileName, appxpackaging/IAppxBundleManifestOptionalBundleInfo::GetFileName, appxpkg.iappxbundlemanifestoptionalbundleinfo_getfilename
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
 - IAppxBundleManifestOptionalBundleInfo::GetFileName
 - appxpackaging/IAppxBundleManifestOptionalBundleInfo::GetFileName
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
 - IAppxBundleManifestOptionalBundleInfo.GetFileName
---

# IAppxBundleManifestOptionalBundleInfo::GetFileName


## -description

Retrieves the file-name attribute of the &lt;OptionalBundle&gt;.

## -parameters

### -param fileName [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a>*</b>

A string that contains the file name of the package.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlemanifestoptionalbundleinfo">IAppxBundleManifestOptionalBundleInfo</a>