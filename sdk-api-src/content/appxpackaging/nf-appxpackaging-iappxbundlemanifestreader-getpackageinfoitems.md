---
UID: NF:appxpackaging.IAppxBundleManifestReader.GetPackageInfoItems
title: IAppxBundleManifestReader::GetPackageInfoItems (appxpackaging.h)
description: Retrieves an enumerator over all the &lt;Package&gt; elements under the &lt;Packages&gt; element.
helpviewer_keywords: ["GetPackageInfoItems","GetPackageInfoItems method [App packaging and management]","GetPackageInfoItems method [App packaging and management]","IAppxBundleManifestReader interface","IAppxBundleManifestReader interface [App packaging and management]","GetPackageInfoItems method","IAppxBundleManifestReader.GetPackageInfoItems","IAppxBundleManifestReader::GetPackageInfoItems","appxpackaging/IAppxBundleManifestReader::GetPackageInfoItems","appxpkg.iappxbundlemanifestreader_getpackageinfoitems"]
old-location: appxpkg\iappxbundlemanifestreader_getpackageinfoitems.htm
tech.root: appxpkg
ms.assetid: D216C27E-5B73-49B5-90A8-11187C129264
ms.date: 12/05/2018
ms.keywords: GetPackageInfoItems, GetPackageInfoItems method [App packaging and management], GetPackageInfoItems method [App packaging and management],IAppxBundleManifestReader interface, IAppxBundleManifestReader interface [App packaging and management],GetPackageInfoItems method, IAppxBundleManifestReader.GetPackageInfoItems, IAppxBundleManifestReader::GetPackageInfoItems, appxpackaging/IAppxBundleManifestReader::GetPackageInfoItems, appxpkg.iappxbundlemanifestreader_getpackageinfoitems
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IAppxBundleManifestReader::GetPackageInfoItems
 - appxpackaging/IAppxBundleManifestReader::GetPackageInfoItems
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
 - IAppxBundleManifestReader.GetPackageInfoItems
---

# IAppxBundleManifestReader::GetPackageInfoItems


## -description

Retrieves an enumerator over all the &lt;Package&gt; elements under the &lt;Packages&gt; element.

## -parameters

### -param packageInfoItems [out, retval]

Type: <b>IAppxBundleManifestPackageInfoEnumerator**</b>

 An enumerator over all payload packages in a &lt;Packages&gt; element of a bundle.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlemanifestreader">IAppxBundleManifestReader</a>