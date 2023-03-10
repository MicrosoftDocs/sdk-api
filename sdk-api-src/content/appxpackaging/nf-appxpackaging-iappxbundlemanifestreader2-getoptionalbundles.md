---
UID: NF:appxpackaging.IAppxBundleManifestReader2.GetOptionalBundles
title: IAppxBundleManifestReader2::GetOptionalBundles (appxpackaging.h)
description: Retrieves an object that represents the &lt;OptionalBundles&gt; element under the root &lt;Bundle&gt; element.
helpviewer_keywords: ["GetOptionalBundles","GetOptionalBundles method [App packaging and management]","GetOptionalBundles method [App packaging and management]","IAppxBundleManifestReader2 interface","IAppxBundleManifestReader2 interface [App packaging and management]","GetOptionalBundles method","IAppxBundleManifestReader2.GetOptionalBundles","IAppxBundleManifestReader2::GetOptionalBundles","appxpackaging/IAppxBundleManifestReader2::GetOptionalBundles","appxpkg.iappxbundlemanifestreader2_getoptionalbundles"]
old-location: appxpkg\iappxbundlemanifestreader2_getoptionalbundles.htm
tech.root: appxpkg
ms.assetid: 26246BB1-7FE7-462F-9731-D8AD32373184
ms.date: 12/05/2018
ms.keywords: GetOptionalBundles, GetOptionalBundles method [App packaging and management], GetOptionalBundles method [App packaging and management],IAppxBundleManifestReader2 interface, IAppxBundleManifestReader2 interface [App packaging and management],GetOptionalBundles method, IAppxBundleManifestReader2.GetOptionalBundles, IAppxBundleManifestReader2::GetOptionalBundles, appxpackaging/IAppxBundleManifestReader2::GetOptionalBundles, appxpkg.iappxbundlemanifestreader2_getoptionalbundles
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
 - IAppxBundleManifestReader2::GetOptionalBundles
 - appxpackaging/IAppxBundleManifestReader2::GetOptionalBundles
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
 - IAppxBundleManifestReader2.GetOptionalBundles
---

# IAppxBundleManifestReader2::GetOptionalBundles


## -description

Retrieves an object that represents the &lt;OptionalBundles&gt; element under the root &lt;Bundle&gt; element.

## -parameters

### -param optionalBundles [out, retval]

The optional bundle.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlemanifestreader2">IAppxBundleManifestReader2</a>