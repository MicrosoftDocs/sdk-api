---
UID: NF:appxpackaging.IAppxBundleManifestOptionalBundleInfoEnumerator.GetCurrent
title: IAppxBundleManifestOptionalBundleInfoEnumerator::GetCurrent (appxpackaging.h)
description: Gets the optional bundle information at the current position of the enumerator.
helpviewer_keywords: ["GetCurrent","GetCurrent method [App packaging and management]","GetCurrent method [App packaging and management]","IAppxBundleManifestOptionalBundleInfoEnumerator interface","IAppxBundleManifestOptionalBundleInfoEnumerator interface [App packaging and management]","GetCurrent method","IAppxBundleManifestOptionalBundleInfoEnumerator.GetCurrent","IAppxBundleManifestOptionalBundleInfoEnumerator::GetCurrent","appxpackaging/IAppxBundleManifestOptionalBundleInfoEnumerator::GetCurrent","appxpkg.iappxbundlemanifestoptionalbundleinfoenumerator_getcurrent"]
old-location: appxpkg\iappxbundlemanifestoptionalbundleinfoenumerator_getcurrent.htm
tech.root: appxpkg
ms.assetid: C9C0E081-52AB-4B7F-B789-EC64B55EFA2A
ms.date: 12/05/2018
ms.keywords: GetCurrent, GetCurrent method [App packaging and management], GetCurrent method [App packaging and management],IAppxBundleManifestOptionalBundleInfoEnumerator interface, IAppxBundleManifestOptionalBundleInfoEnumerator interface [App packaging and management],GetCurrent method, IAppxBundleManifestOptionalBundleInfoEnumerator.GetCurrent, IAppxBundleManifestOptionalBundleInfoEnumerator::GetCurrent, appxpackaging/IAppxBundleManifestOptionalBundleInfoEnumerator::GetCurrent, appxpkg.iappxbundlemanifestoptionalbundleinfoenumerator_getcurrent
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
 - IAppxBundleManifestOptionalBundleInfoEnumerator::GetCurrent
 - appxpackaging/IAppxBundleManifestOptionalBundleInfoEnumerator::GetCurrent
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
 - IAppxBundleManifestOptionalBundleInfoEnumerator.GetCurrent
---

# IAppxBundleManifestOptionalBundleInfoEnumerator::GetCurrent


## -description

Gets the optional bundle information at the current position of the enumerator.

## -parameters

### -param optionalBundle [out, retval]

The optional bundle information.

## -returns

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

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxbundlemanifestoptionalbundleinfoenumerator">IAppxBundleManifestOptionalBundleInfoEnumerator</a>