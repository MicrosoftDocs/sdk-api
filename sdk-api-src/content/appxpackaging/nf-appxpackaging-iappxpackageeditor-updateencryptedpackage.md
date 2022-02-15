---
UID: NF:appxpackaging.IAppxPackageEditor.UpdateEncryptedPackage
title: IAppxPackageEditor::UpdateEncryptedPackage (appxpackaging.h)
description: Updates an encrypted app package.
helpviewer_keywords: ["IAppxPackageEditor interface [App packaging and management]","UpdateEncryptedPackage method","IAppxPackageEditor.UpdateEncryptedPackage","IAppxPackageEditor::UpdateEncryptedPackage","UpdateEncryptedPackage","UpdateEncryptedPackage method [App packaging and management]","UpdateEncryptedPackage method [App packaging and management]","IAppxPackageEditor interface","appxpackaging/IAppxPackageEditor::UpdateEncryptedPackage","appxpkg.iappxpackageeditor_updateencryptedpackage"]
old-location: appxpkg\iappxpackageeditor_updateencryptedpackage.htm
tech.root: appxpkg
ms.assetid: 4D5E2F4B-00CE-4A0A-A514-3B66EC3065ED
ms.date: 12/05/2018
ms.keywords: IAppxPackageEditor interface [App packaging and management],UpdateEncryptedPackage method, IAppxPackageEditor.UpdateEncryptedPackage, IAppxPackageEditor::UpdateEncryptedPackage, UpdateEncryptedPackage, UpdateEncryptedPackage method [App packaging and management], UpdateEncryptedPackage method [App packaging and management],IAppxPackageEditor interface, appxpackaging/IAppxPackageEditor::UpdateEncryptedPackage, appxpkg.iappxpackageeditor_updateencryptedpackage
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
 - IAppxPackageEditor::UpdateEncryptedPackage
 - appxpackaging/IAppxPackageEditor::UpdateEncryptedPackage
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
 - IAppxPackageEditor.UpdateEncryptedPackage
---

# IAppxPackageEditor::UpdateEncryptedPackage


## -description

Updates an encrypted app package.

## -parameters

### -param baselineEncryptedPackageStream [in]

An <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> that provides the contents of the baseline encrypted app package.

### -param deltaPackageStream [in]

An <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> that provides the contents of the delta (difference) app package.

### -param updateOption [in]

The update options.

### -param settings [in]

The encrypted app package settings.

### -param keyInfo [in]

App package key information.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxpackageeditor">IAppxPackageEditor</a>