---
UID: NF:appxpackaging.IAppxManifestApplicationsEnumerator.GetCurrent
title: IAppxManifestApplicationsEnumerator::GetCurrent (appxpackaging.h)
description: Gets the application at the current position of the enumerator.
helpviewer_keywords: ["GetCurrent","GetCurrent method [App packaging and management]","GetCurrent method [App packaging and management]","IAppxManifestApplicationsEnumerator interface","IAppxManifestApplicationsEnumerator interface [App packaging and management]","GetCurrent method","IAppxManifestApplicationsEnumerator.GetCurrent","IAppxManifestApplicationsEnumerator::GetCurrent","appxpackaging/IAppxManifestApplicationsEnumerator::GetCurrent","appxpkg.iappxmanifestapplicationsenumerator_getcurrent"]
old-location: appxpkg\iappxmanifestapplicationsenumerator_getcurrent.htm
tech.root: appxpkg
ms.assetid: 54357408-57EA-4BD0-A619-F297C6248050
ms.date: 12/05/2018
ms.keywords: GetCurrent, GetCurrent method [App packaging and management], GetCurrent method [App packaging and management],IAppxManifestApplicationsEnumerator interface, IAppxManifestApplicationsEnumerator interface [App packaging and management],GetCurrent method, IAppxManifestApplicationsEnumerator.GetCurrent, IAppxManifestApplicationsEnumerator::GetCurrent, appxpackaging/IAppxManifestApplicationsEnumerator::GetCurrent, appxpkg.iappxmanifestapplicationsenumerator_getcurrent
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
 - IAppxManifestApplicationsEnumerator::GetCurrent
 - appxpackaging/IAppxManifestApplicationsEnumerator::GetCurrent
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
 - IAppxManifestApplicationsEnumerator.GetCurrent
---

# IAppxManifestApplicationsEnumerator::GetCurrent


## -description

Gets the application at the current position of the enumerator.

## -parameters

### -param application [out, retval]

Type: <b><a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestapplication">IAppxManifestApplication</a>**</b>

The current application.

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

The enumerator returned can be empty. In this case, a call to  <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestapplicationsenumerator-gethascurrent">GetHasCurrent</a> returns <b>false</b>. If the enumerator is not empty, it points to the first element, and this method returns the first item. Subsequently, the user should use <a href="/windows/desktop/api/appxpackaging/nf-appxpackaging-iappxmanifestapplicationsenumerator-movenext">MoveNext</a> to move through the items, and call <b>GetHasCurrent</b> before using <b>GetCurrent</b> to access the item.


#### Examples

For an example, see <a href="/windows/desktop/appxpkg/how-to-query-package-identity-information">Quickstart: Read app package manifest info</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestapplicationsenumerator">IAppxManifestApplicationsEnumerator</a>