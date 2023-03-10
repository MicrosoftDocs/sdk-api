---
UID: NF:appxpackaging.IAppxPackageEditor.UpdatePackageManifest
title: IAppxPackageEditor::UpdatePackageManifest (appxpackaging.h)
description: Updates an app package manifest.
helpviewer_keywords: ["IAppxPackageEditor interface [App packaging and management]","UpdatePackageManifest method","IAppxPackageEditor.UpdatePackageManifest","IAppxPackageEditor::UpdatePackageManifest","UpdatePackageManifest","UpdatePackageManifest method [App packaging and management]","UpdatePackageManifest method [App packaging and management]","IAppxPackageEditor interface","appxpackaging/IAppxPackageEditor::UpdatePackageManifest","appxpkg.iappxpackageeditor_updatepackagemanifest"]
old-location: appxpkg\iappxpackageeditor_updatepackagemanifest.htm
tech.root: appxpkg
ms.assetid: A30B3A7E-28FA-4780-9ED3-4F19887189E8
ms.date: 12/05/2018
ms.keywords: IAppxPackageEditor interface [App packaging and management],UpdatePackageManifest method, IAppxPackageEditor.UpdatePackageManifest, IAppxPackageEditor::UpdatePackageManifest, UpdatePackageManifest, UpdatePackageManifest method [App packaging and management], UpdatePackageManifest method [App packaging and management],IAppxPackageEditor interface, appxpackaging/IAppxPackageEditor::UpdatePackageManifest, appxpkg.iappxpackageeditor_updatepackagemanifest
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
 - IAppxPackageEditor::UpdatePackageManifest
 - appxpackaging/IAppxPackageEditor::UpdatePackageManifest
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
 - IAppxPackageEditor.UpdatePackageManifest
---

# IAppxPackageEditor::UpdatePackageManifest


## -description

Updates an app package manifest.

## -parameters

### -param packageStream [in]

An <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> that provides the contents of the app package associated with the manifest to be updated.

### -param updatedManifestStream [in]

An <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> that provides the contents of the updated app package manifest.

### -param isPackageEncrypted [in]

Flag to specify whether the package is encrypted.

### -param options [in]

Options for app package manifest validation.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxpackageeditor">IAppxPackageEditor</a>