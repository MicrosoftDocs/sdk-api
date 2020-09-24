---
UID: NF:appxpackaging.IAppxManifestResourcesEnumerator.MoveNext
title: IAppxManifestResourcesEnumerator::MoveNext (appxpackaging.h)
description: Advances the position of the enumerator to the next resource.
helpviewer_keywords: ["IAppxManifestResourcesEnumerator interface [App packaging and management]","MoveNext method","IAppxManifestResourcesEnumerator.MoveNext","IAppxManifestResourcesEnumerator::MoveNext","MoveNext","MoveNext method [App packaging and management]","MoveNext method [App packaging and management]","IAppxManifestResourcesEnumerator interface","appxpackaging/IAppxManifestResourcesEnumerator::MoveNext","appxpkg.iappxmanifestresourcesenumerator_movenext"]
old-location: appxpkg\iappxmanifestresourcesenumerator_movenext.htm
tech.root: appxpkg
ms.assetid: CD5A7FF9-A28E-4857-AE7B-92F8EEBA0235
ms.date: 12/05/2018
ms.keywords: IAppxManifestResourcesEnumerator interface [App packaging and management],MoveNext method, IAppxManifestResourcesEnumerator.MoveNext, IAppxManifestResourcesEnumerator::MoveNext, MoveNext, MoveNext method [App packaging and management], MoveNext method [App packaging and management],IAppxManifestResourcesEnumerator interface, appxpackaging/IAppxManifestResourcesEnumerator::MoveNext, appxpkg.iappxmanifestresourcesenumerator_movenext
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
 - IAppxManifestResourcesEnumerator::MoveNext
 - appxpackaging/IAppxManifestResourcesEnumerator::MoveNext
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
 - IAppxManifestResourcesEnumerator.MoveNext
---

# IAppxManifestResourcesEnumerator::MoveNext


## -description

Advances the position of the enumerator to the next resource.

## -parameters

### -param hasNext [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

<b>TRUE</b> if the enumerator successfully advances

<b>FALSE</b> if the enumerator has passed the end of the collection.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code.

Note that when the enumerator passes the end of the collection for the first time, <i>hasNext</i> = <b>FALSE</b>,  but the method succeeds and returns <b>S_OK</b>. However, the method returns <b>E_BOUNDS</b> if you subsequently call another MoveNext after you have already passed the end of the collection, and you have previously received  <i>hasNext</i> = <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestresourcesenumerator">IAppxManifestResourcesEnumerator</a>