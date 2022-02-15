---
UID: NF:appxpackaging.IAppxManifestResourcesEnumerator.GetHasCurrent
title: IAppxManifestResourcesEnumerator::GetHasCurrent (appxpackaging.h)
description: Determines whether there is a resource at the current position of the enumerator.
helpviewer_keywords: ["GetHasCurrent","GetHasCurrent method [App packaging and management]","GetHasCurrent method [App packaging and management]","IAppxManifestResourcesEnumerator interface","IAppxManifestResourcesEnumerator interface [App packaging and management]","GetHasCurrent method","IAppxManifestResourcesEnumerator.GetHasCurrent","IAppxManifestResourcesEnumerator::GetHasCurrent","appxpackaging/IAppxManifestResourcesEnumerator::GetHasCurrent","appxpkg.iappxmanifestresourcesenumerator_gethascurrent"]
old-location: appxpkg\iappxmanifestresourcesenumerator_gethascurrent.htm
tech.root: appxpkg
ms.assetid: 72798FDF-3296-4AC7-9BA0-212457F9BEC7
ms.date: 12/05/2018
ms.keywords: GetHasCurrent, GetHasCurrent method [App packaging and management], GetHasCurrent method [App packaging and management],IAppxManifestResourcesEnumerator interface, IAppxManifestResourcesEnumerator interface [App packaging and management],GetHasCurrent method, IAppxManifestResourcesEnumerator.GetHasCurrent, IAppxManifestResourcesEnumerator::GetHasCurrent, appxpackaging/IAppxManifestResourcesEnumerator::GetHasCurrent, appxpkg.iappxmanifestresourcesenumerator_gethascurrent
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
 - IAppxManifestResourcesEnumerator::GetHasCurrent
 - appxpackaging/IAppxManifestResourcesEnumerator::GetHasCurrent
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
 - IAppxManifestResourcesEnumerator.GetHasCurrent
---

# IAppxManifestResourcesEnumerator::GetHasCurrent


## -description

Determines whether there is a resource at the current position of the enumerator.

## -parameters

### -param hasCurrent [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

<b>TRUE</b> if the enumerator's current position references an item; <b>FALSE</b> if the enumerator has passed the last item in the collection.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestresourcesenumerator">IAppxManifestResourcesEnumerator</a>