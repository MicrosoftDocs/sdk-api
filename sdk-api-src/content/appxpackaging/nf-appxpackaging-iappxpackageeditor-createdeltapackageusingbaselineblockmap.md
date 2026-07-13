---
UID: NF:appxpackaging.IAppxPackageEditor.CreateDeltaPackageUsingBaselineBlockMap
title: IAppxPackageEditor::CreateDeltaPackageUsingBaselineBlockMap (appxpackaging.h)
description: Creates a delta package from the differences in the updated package and the baseline block map.
helpviewer_keywords: ["CreateDeltaPackageUsingBaselineBlockMap","CreateDeltaPackageUsingBaselineBlockMap method [App packaging and management]","CreateDeltaPackageUsingBaselineBlockMap method [App packaging and management]","IAppxPackageEditor interface","IAppxPackageEditor interface [App packaging and management]","CreateDeltaPackageUsingBaselineBlockMap method","IAppxPackageEditor.CreateDeltaPackageUsingBaselineBlockMap","IAppxPackageEditor::CreateDeltaPackageUsingBaselineBlockMap","appxpackaging/IAppxPackageEditor::CreateDeltaPackageUsingBaselineBlockMap","appxpkg.iappxpackageeditor_createdeltapackageusingbaselineblockmap"]
old-location: appxpkg\iappxpackageeditor_createdeltapackageusingbaselineblockmap.htm
tech.root: appxpkg
ms.assetid: 33D1CEBA-A7F4-4506-B467-3610A3737B87
ms.date: 12/05/2018
ms.keywords: CreateDeltaPackageUsingBaselineBlockMap, CreateDeltaPackageUsingBaselineBlockMap method [App packaging and management], CreateDeltaPackageUsingBaselineBlockMap method [App packaging and management],IAppxPackageEditor interface, IAppxPackageEditor interface [App packaging and management],CreateDeltaPackageUsingBaselineBlockMap method, IAppxPackageEditor.CreateDeltaPackageUsingBaselineBlockMap, IAppxPackageEditor::CreateDeltaPackageUsingBaselineBlockMap, appxpackaging/IAppxPackageEditor::CreateDeltaPackageUsingBaselineBlockMap, appxpkg.iappxpackageeditor_createdeltapackageusingbaselineblockmap
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
 - IAppxPackageEditor::CreateDeltaPackageUsingBaselineBlockMap
 - appxpackaging/IAppxPackageEditor::CreateDeltaPackageUsingBaselineBlockMap
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
 - IAppxPackageEditor.CreateDeltaPackageUsingBaselineBlockMap
---

# IAppxPackageEditor::CreateDeltaPackageUsingBaselineBlockMap


## -description

Creates a delta package from the differences in the updated package and the baseline block map.

## -parameters

### -param updatedPackageStream [in]

An <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> that provides the contents of the updated app package.

### -param baselineBlockMapStream [in]

An <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> that provides the contents of the baseline block map.

### -param baselinePackageFullName [in]

The full name of the baseline app package.

### -param deltaPackageStream [in]

An <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> that provides the contents of the delta (difference) app package.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxpackageeditor">IAppxPackageEditor</a>