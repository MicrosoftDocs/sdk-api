---
UID: NF:appxpackaging.IAppxBundleManifestPackageInfo.GetResources
title: IAppxBundleManifestPackageInfo::GetResources (appxpackaging.h)
description: Retrieves an enumerator that iterates through all the &lt;Resource&gt; elements that are defined in the app package's manifest.
helpviewer_keywords: ["GetResources","GetResources method [App packaging and management]","GetResources method [App packaging and management]","IAppxBundleManifestPackageInfo interface","IAppxBundleManifestPackageInfo interface [App packaging and management]","GetResources method","IAppxBundleManifestPackageInfo.GetResources","IAppxBundleManifestPackageInfo::GetResources","appxpackaging/IAppxBundleManifestPackageInfo::GetResources","appxpkg.iappxbundlemanifestpackageinfo_getresources"]
old-location: appxpkg\iappxbundlemanifestpackageinfo_getresources.htm
tech.root: appxpkg
ms.assetid: 07B1028B-4084-44E5-840D-14403E01F628
ms.date: 12/05/2018
ms.keywords: GetResources, GetResources method [App packaging and management], GetResources method [App packaging and management],IAppxBundleManifestPackageInfo interface, IAppxBundleManifestPackageInfo interface [App packaging and management],GetResources method, IAppxBundleManifestPackageInfo.GetResources, IAppxBundleManifestPackageInfo::GetResources, appxpackaging/IAppxBundleManifestPackageInfo::GetResources, appxpkg.iappxbundlemanifestpackageinfo_getresources
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
 - IAppxBundleManifestPackageInfo::GetResources
 - appxpackaging/IAppxBundleManifestPackageInfo::GetResources
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
 - IAppxBundleManifestPackageInfo.GetResources
---

# IAppxBundleManifestPackageInfo::GetResources


## -description

Retrieves an enumerator that iterates through all the &lt;Resource&gt; elements that are defined in the app package's manifest.

## -parameters

### -param resources [out, retval]

Type: <b><a href="/previous-versions/dn280306(v=vs.85)">IAppxManifestQualifiedResourcesEnumerator</a>**</b>

The enumerator that iterates through the resources.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlemanifestpackageinfo">IAppxBundleManifestPackageInfo</a>