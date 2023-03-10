---
UID: NF:appxpackaging.IAppxBundleManifestPackageInfoEnumerator.GetHasCurrent
title: IAppxBundleManifestPackageInfoEnumerator::GetHasCurrent (appxpackaging.h)
description: Determines whether there are more elements in the enumerator.
helpviewer_keywords: ["GetHasCurrent","GetHasCurrent method [App packaging and management]","GetHasCurrent method [App packaging and management]","IAppxBundleManifestPackageInfoEnumerator interface","IAppxBundleManifestPackageInfoEnumerator interface [App packaging and management]","GetHasCurrent method","IAppxBundleManifestPackageInfoEnumerator.GetHasCurrent","IAppxBundleManifestPackageInfoEnumerator::GetHasCurrent","appxpackaging/IAppxBundleManifestPackageInfoEnumerator::GetHasCurrent","appxpkg.iappxbundlemanifestpackageinfoenumerator_gethascurrent"]
old-location: appxpkg\iappxbundlemanifestpackageinfoenumerator_gethascurrent.htm
tech.root: appxpkg
ms.assetid: ED12F498-1F8D-45B2-9CFE-7215D2D87C3F
ms.date: 12/05/2018
ms.keywords: GetHasCurrent, GetHasCurrent method [App packaging and management], GetHasCurrent method [App packaging and management],IAppxBundleManifestPackageInfoEnumerator interface, IAppxBundleManifestPackageInfoEnumerator interface [App packaging and management],GetHasCurrent method, IAppxBundleManifestPackageInfoEnumerator.GetHasCurrent, IAppxBundleManifestPackageInfoEnumerator::GetHasCurrent, appxpackaging/IAppxBundleManifestPackageInfoEnumerator::GetHasCurrent, appxpkg.iappxbundlemanifestpackageinfoenumerator_gethascurrent
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
 - IAppxBundleManifestPackageInfoEnumerator::GetHasCurrent
 - appxpackaging/IAppxBundleManifestPackageInfoEnumerator::GetHasCurrent
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
 - IAppxBundleManifestPackageInfoEnumerator.GetHasCurrent
---

# IAppxBundleManifestPackageInfoEnumerator::GetHasCurrent


## -description

Determines whether there are more elements in the enumerator.

## -parameters

### -param hasCurrent [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

<b>TRUE</b> if the enumerator's current position references an item; <b>FALSE</b> if the enumerator has passed the last item in the collection.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlemanifestpackageinfoenumerator">IAppxBundleManifestPackageInfoEnumerator</a>