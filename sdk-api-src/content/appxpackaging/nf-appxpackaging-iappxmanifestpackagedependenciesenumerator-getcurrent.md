---
UID: NF:appxpackaging.IAppxManifestPackageDependenciesEnumerator.GetCurrent
title: IAppxManifestPackageDependenciesEnumerator::GetCurrent (appxpackaging.h)
description: Gets the dependency package at the current position of the enumerator.
helpviewer_keywords: ["GetCurrent","GetCurrent method [App packaging and management]","GetCurrent method [App packaging and management]","IAppxManifestPackageDependenciesEnumerator interface","IAppxManifestPackageDependenciesEnumerator interface [App packaging and management]","GetCurrent method","IAppxManifestPackageDependenciesEnumerator.GetCurrent","IAppxManifestPackageDependenciesEnumerator::GetCurrent","appxpackaging/IAppxManifestPackageDependenciesEnumerator::GetCurrent","appxpkg.iappxmanifestpackagedependenciesenumerator_getcurrent"]
old-location: appxpkg\iappxmanifestpackagedependenciesenumerator_getcurrent.htm
tech.root: appxpkg
ms.assetid: A7DDD037-2A0B-485A-AF1E-7A999780496B
ms.date: 12/05/2018
ms.keywords: GetCurrent, GetCurrent method [App packaging and management], GetCurrent method [App packaging and management],IAppxManifestPackageDependenciesEnumerator interface, IAppxManifestPackageDependenciesEnumerator interface [App packaging and management],GetCurrent method, IAppxManifestPackageDependenciesEnumerator.GetCurrent, IAppxManifestPackageDependenciesEnumerator::GetCurrent, appxpackaging/IAppxManifestPackageDependenciesEnumerator::GetCurrent, appxpkg.iappxmanifestpackagedependenciesenumerator_getcurrent
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
 - IAppxManifestPackageDependenciesEnumerator::GetCurrent
 - appxpackaging/IAppxManifestPackageDependenciesEnumerator::GetCurrent
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
 - IAppxManifestPackageDependenciesEnumerator.GetCurrent
---

# IAppxManifestPackageDependenciesEnumerator::GetCurrent


## -description

Gets the dependency package at the current position of the enumerator.

## -parameters

### -param dependency [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestpackagedependency">IAppxManifestPackageDependency</a>**</b>

The current dependency package.

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

The enumerator returned can be empty. In this case, a call to  <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestpackagedependenciesenumerator-gethascurrent">GetHasCurrent</a> returns <b>false</b>. If the enumerator is not empty, it points to the first element, and this method returns the first item. Subsequently, the user should use <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestpackagedependenciesenumerator-movenext">MoveNext</a> to move through the items, and call <b>GetHasCurrent</b> before using <b>GetCurrent</b> to access the item.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestpackagedependenciesenumerator">IAppxManifestPackageDependenciesEnumerator</a>