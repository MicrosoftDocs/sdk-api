---
UID: NF:appxpackaging.IAppxBundleManifestPackageInfoEnumerator.MoveNext
title: IAppxBundleManifestPackageInfoEnumerator::MoveNext (appxpackaging.h)
description: Advances the position of the enumerator to the next &lt;Package&gt; element.
helpviewer_keywords: ["IAppxBundleManifestPackageInfoEnumerator interface [App packaging and management]","MoveNext method","IAppxBundleManifestPackageInfoEnumerator.MoveNext","IAppxBundleManifestPackageInfoEnumerator::MoveNext","MoveNext","MoveNext method [App packaging and management]","MoveNext method [App packaging and management]","IAppxBundleManifestPackageInfoEnumerator interface","appxpackaging/IAppxBundleManifestPackageInfoEnumerator::MoveNext","appxpkg.iappxbundlemanifestpackageinfoenumerator_movenext"]
old-location: appxpkg\iappxbundlemanifestpackageinfoenumerator_movenext.htm
tech.root: appxpkg
ms.assetid: 8818FC6B-28CB-420F-A5BB-BCB62DFD4A78
ms.date: 12/05/2018
ms.keywords: IAppxBundleManifestPackageInfoEnumerator interface [App packaging and management],MoveNext method, IAppxBundleManifestPackageInfoEnumerator.MoveNext, IAppxBundleManifestPackageInfoEnumerator::MoveNext, MoveNext, MoveNext method [App packaging and management], MoveNext method [App packaging and management],IAppxBundleManifestPackageInfoEnumerator interface, appxpackaging/IAppxBundleManifestPackageInfoEnumerator::MoveNext, appxpkg.iappxbundlemanifestpackageinfoenumerator_movenext
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
 - IAppxBundleManifestPackageInfoEnumerator::MoveNext
 - appxpackaging/IAppxBundleManifestPackageInfoEnumerator::MoveNext
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
 - IAppxBundleManifestPackageInfoEnumerator.MoveNext
---

# IAppxBundleManifestPackageInfoEnumerator::MoveNext


## -description

Advances the position of the enumerator to the next &lt;Package&gt; element.

## -parameters

### -param hasNext [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

<b>TRUE</b> if the enumerator successfully advances

<b>FALSE</b> if the enumerator has passed the end of the collection.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code.

<div class="alert"><b>Note</b>  When the enumerator passes the end of the collection for the first time, <i>hasNext</i> = <b>FALSE</b>,  but the method succeeds and returns <b>S_OK</b>. However, the method returns <b>E_BOUNDS</b> if you subsequently call another <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestapplicationsenumerator-movenext">MoveNext</a> after you have already passed the end of the collection, and you have previously received  <i>hasNext</i> = <b>FALSE</b>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlemanifestpackageinfoenumerator">IAppxBundleManifestPackageInfoEnumerator</a>