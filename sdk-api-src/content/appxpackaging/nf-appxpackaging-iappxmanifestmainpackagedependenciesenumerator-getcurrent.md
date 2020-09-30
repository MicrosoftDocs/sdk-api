---
UID: NF:appxpackaging.IAppxManifestMainPackageDependenciesEnumerator.GetCurrent
title: IAppxManifestMainPackageDependenciesEnumerator::GetCurrent (appxpackaging.h)
description: Gets the &lt;MainPackageDependency&gt; element at the current position of the enumerator.
helpviewer_keywords: ["GetCurrent","GetCurrent method [App packaging and management]","GetCurrent method [App packaging and management]","IAppxManifestMainPackageDependenciesEnumerator interface","IAppxManifestMainPackageDependenciesEnumerator interface [App packaging and management]","GetCurrent method","IAppxManifestMainPackageDependenciesEnumerator.GetCurrent","IAppxManifestMainPackageDependenciesEnumerator::GetCurrent","appxpackaging/IAppxManifestMainPackageDependenciesEnumerator::GetCurrent","appxpkg.iappxmanifestmainpackagedependenciesenumerator_getcurrent"]
old-location: appxpkg\iappxmanifestmainpackagedependenciesenumerator_getcurrent.htm
tech.root: appxpkg
ms.assetid: 14C7F3F9-38FE-4FC2-9255-0A728A1488C0
ms.date: 12/05/2018
ms.keywords: GetCurrent, GetCurrent method [App packaging and management], GetCurrent method [App packaging and management],IAppxManifestMainPackageDependenciesEnumerator interface, IAppxManifestMainPackageDependenciesEnumerator interface [App packaging and management],GetCurrent method, IAppxManifestMainPackageDependenciesEnumerator.GetCurrent, IAppxManifestMainPackageDependenciesEnumerator::GetCurrent, appxpackaging/IAppxManifestMainPackageDependenciesEnumerator::GetCurrent, appxpkg.iappxmanifestmainpackagedependenciesenumerator_getcurrent
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
 - IAppxManifestMainPackageDependenciesEnumerator::GetCurrent
 - appxpackaging/IAppxManifestMainPackageDependenciesEnumerator::GetCurrent
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
 - IAppxManifestMainPackageDependenciesEnumerator.GetCurrent
---

# IAppxManifestMainPackageDependenciesEnumerator::GetCurrent


## -description

Gets the &lt;MainPackageDependency&gt; element at the current position of the enumerator.

## -parameters

### -param mainPackageDependency [out, retval]

The current &lt;MainPackageDependency&gt; element.

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

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestmainpackagedependenciesenumerator">IAppxManifestMainPackageDependenciesEnumerator</a>