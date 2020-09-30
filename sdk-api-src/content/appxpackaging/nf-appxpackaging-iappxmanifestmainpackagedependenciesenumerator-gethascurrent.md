---
UID: NF:appxpackaging.IAppxManifestMainPackageDependenciesEnumerator.GetHasCurrent
title: IAppxManifestMainPackageDependenciesEnumerator::GetHasCurrent (appxpackaging.h)
description: Determines whether there is a &lt;MainPackageDependency&gt; element at the current position of the enumerator.
helpviewer_keywords: ["GetHasCurrent","GetHasCurrent method [App packaging and management]","GetHasCurrent method [App packaging and management]","IAppxManifestMainPackageDependenciesEnumerator interface","IAppxManifestMainPackageDependenciesEnumerator interface [App packaging and management]","GetHasCurrent method","IAppxManifestMainPackageDependenciesEnumerator.GetHasCurrent","IAppxManifestMainPackageDependenciesEnumerator::GetHasCurrent","appxpackaging/IAppxManifestMainPackageDependenciesEnumerator::GetHasCurrent","appxpkg.iappxmanifestmainpackagedependenciesenumerator_gethascurrent"]
old-location: appxpkg\iappxmanifestmainpackagedependenciesenumerator_gethascurrent.htm
tech.root: appxpkg
ms.assetid: DB350E8E-8A0B-4742-B7E3-2133603A0714
ms.date: 12/05/2018
ms.keywords: GetHasCurrent, GetHasCurrent method [App packaging and management], GetHasCurrent method [App packaging and management],IAppxManifestMainPackageDependenciesEnumerator interface, IAppxManifestMainPackageDependenciesEnumerator interface [App packaging and management],GetHasCurrent method, IAppxManifestMainPackageDependenciesEnumerator.GetHasCurrent, IAppxManifestMainPackageDependenciesEnumerator::GetHasCurrent, appxpackaging/IAppxManifestMainPackageDependenciesEnumerator::GetHasCurrent, appxpkg.iappxmanifestmainpackagedependenciesenumerator_gethascurrent
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
 - IAppxManifestMainPackageDependenciesEnumerator::GetHasCurrent
 - appxpackaging/IAppxManifestMainPackageDependenciesEnumerator::GetHasCurrent
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
 - IAppxManifestMainPackageDependenciesEnumerator.GetHasCurrent
---

# IAppxManifestMainPackageDependenciesEnumerator::GetHasCurrent


## -description

Determines whether there is a &lt;MainPackageDependency&gt; element at the current position of the enumerator.

## -parameters

### -param hasCurrent [out, retval]

<b>TRUE</b> if the enumerator's current position references an item; <b>FALSE</b> if the enumerator has passed the last item in the collection.

## -returns

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxmanifestmainpackagedependenciesenumerator">IAppxManifestMainPackageDependenciesEnumerator</a>