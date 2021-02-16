---
UID: NF:appxpackaging.IAppxBundleManifestPackageInfoEnumerator.GetCurrent
title: IAppxBundleManifestPackageInfoEnumerator::GetCurrent (appxpackaging.h)
description: Gets the &lt;Package&gt; element at the current position of the enumerator.
helpviewer_keywords: ["GetCurrent","GetCurrent method [App packaging and management]","GetCurrent method [App packaging and management]","IAppxBundleManifestPackageInfoEnumerator interface","IAppxBundleManifestPackageInfoEnumerator interface [App packaging and management]","GetCurrent method","IAppxBundleManifestPackageInfoEnumerator.GetCurrent","IAppxBundleManifestPackageInfoEnumerator::GetCurrent","appxpackaging/IAppxBundleManifestPackageInfoEnumerator::GetCurrent","appxpkg.iappxbundlemanifestpackageinfoenumerator_getcurrent"]
old-location: appxpkg\iappxbundlemanifestpackageinfoenumerator_getcurrent.htm
tech.root: appxpkg
ms.assetid: 52F525CB-162B-47E9-BF85-B920CBCCD983
ms.date: 12/05/2018
ms.keywords: GetCurrent, GetCurrent method [App packaging and management], GetCurrent method [App packaging and management],IAppxBundleManifestPackageInfoEnumerator interface, IAppxBundleManifestPackageInfoEnumerator interface [App packaging and management],GetCurrent method, IAppxBundleManifestPackageInfoEnumerator.GetCurrent, IAppxBundleManifestPackageInfoEnumerator::GetCurrent, appxpackaging/IAppxBundleManifestPackageInfoEnumerator::GetCurrent, appxpkg.iappxbundlemanifestpackageinfoenumerator_getcurrent
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
 - IAppxBundleManifestPackageInfoEnumerator::GetCurrent
 - appxpackaging/IAppxBundleManifestPackageInfoEnumerator::GetCurrent
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
 - IAppxBundleManifestPackageInfoEnumerator.GetCurrent
---

# IAppxBundleManifestPackageInfoEnumerator::GetCurrent


## -description

Gets the &lt;Package&gt; element at the current position of the enumerator.

## -parameters

### -param packageInfo [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlemanifestpackageinfo">IAppxBundleManifestPackageInfo</a>**</b>

The current &lt;Package&gt; element.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code that includes, but is not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
The enumerator has passed the last item in the collection.

</td>
</tr>
</table>

## -remarks

The enumerator’s position points to the first element by default. So, with a newly constructed enumerator that contains at least one element, <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxbundlemanifestpackageinfoenumerator-gethascurrent">IAppxBundleManifestPackageInfoEnumerator::GetHasCurrent</a> returns <b>TRUE</b> and <b>GetCurrent</b> returns the first element.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlemanifestpackageinfoenumerator">IAppxBundleManifestPackageInfoEnumerator</a>