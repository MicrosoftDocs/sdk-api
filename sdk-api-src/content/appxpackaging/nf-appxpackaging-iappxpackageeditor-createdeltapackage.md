---
UID: NF:appxpackaging.IAppxPackageEditor.CreateDeltaPackage
title: IAppxPackageEditor::CreateDeltaPackage (appxpackaging.h)
description: Creates a delta package from the differences in the updated package and the baseline package.
helpviewer_keywords: ["CreateDeltaPackage","CreateDeltaPackage method [App packaging and management]","CreateDeltaPackage method [App packaging and management]","IAppxPackageEditor interface","IAppxPackageEditor interface [App packaging and management]","CreateDeltaPackage method","IAppxPackageEditor.CreateDeltaPackage","IAppxPackageEditor::CreateDeltaPackage","appxpackaging/IAppxPackageEditor::CreateDeltaPackage","appxpkg.iappxpackageeditor_createdeltapackage"]
old-location: appxpkg\iappxpackageeditor_createdeltapackage.htm
tech.root: appxpkg
ms.assetid: 40B41D47-674A-4842-8C6D-FBB661D12589
ms.date: 12/05/2018
ms.keywords: CreateDeltaPackage, CreateDeltaPackage method [App packaging and management], CreateDeltaPackage method [App packaging and management],IAppxPackageEditor interface, IAppxPackageEditor interface [App packaging and management],CreateDeltaPackage method, IAppxPackageEditor.CreateDeltaPackage, IAppxPackageEditor::CreateDeltaPackage, appxpackaging/IAppxPackageEditor::CreateDeltaPackage, appxpkg.iappxpackageeditor_createdeltapackage
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
 - IAppxPackageEditor::CreateDeltaPackage
 - appxpackaging/IAppxPackageEditor::CreateDeltaPackage
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
 - IAppxPackageEditor.CreateDeltaPackage
---

# IAppxPackageEditor::CreateDeltaPackage


## -description

Creates a delta package from the differences in the updated package and the baseline package.

## -parameters

### -param updatedPackageStream [in]

An <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> that provides the contents of the updated app package.

### -param baselinePackageStream [in]

An <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> that provides the contents of the baseline app package.

### -param deltaPackageStream [in]

An <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> that provides the contents of the delta (difference) app package.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxpackageeditor">IAppxPackageEditor</a>