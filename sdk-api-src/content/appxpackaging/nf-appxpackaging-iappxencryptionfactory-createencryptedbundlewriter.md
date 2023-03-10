---
UID: NF:appxpackaging.IAppxEncryptionFactory.CreateEncryptedBundleWriter
title: IAppxEncryptionFactory::CreateEncryptedBundleWriter (appxpackaging.h)
description: Creates a write-only bundle object to which encrypted Windows app packages can be added. (IAppxEncryptionFactory.CreateEncryptedBundleWriter)
helpviewer_keywords: ["CreateEncryptedBundleWriter","CreateEncryptedBundleWriter method [App packaging and management]","CreateEncryptedBundleWriter method [App packaging and management]","IAppxEncryptionFactory interface","IAppxEncryptionFactory interface [App packaging and management]","CreateEncryptedBundleWriter method","IAppxEncryptionFactory.CreateEncryptedBundleWriter","IAppxEncryptionFactory::CreateEncryptedBundleWriter","appxpackaging/IAppxEncryptionFactory::CreateEncryptedBundleWriter","appxpkg.iappxencryptionfactory_createencryptedbundlewriter"]
old-location: appxpkg\iappxencryptionfactory_createencryptedbundlewriter.htm
tech.root: appxpkg
ms.assetid: 01FF3DF1-CCA8-49BF-9876-57A4DDA658D0
ms.date: 12/05/2018
ms.keywords: CreateEncryptedBundleWriter, CreateEncryptedBundleWriter method [App packaging and management], CreateEncryptedBundleWriter method [App packaging and management],IAppxEncryptionFactory interface, IAppxEncryptionFactory interface [App packaging and management],CreateEncryptedBundleWriter method, IAppxEncryptionFactory.CreateEncryptedBundleWriter, IAppxEncryptionFactory::CreateEncryptedBundleWriter, appxpackaging/IAppxEncryptionFactory::CreateEncryptedBundleWriter, appxpkg.iappxencryptionfactory_createencryptedbundlewriter
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
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
 - IAppxEncryptionFactory::CreateEncryptedBundleWriter
 - appxpackaging/IAppxEncryptionFactory::CreateEncryptedBundleWriter
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
 - IAppxEncryptionFactory.CreateEncryptedBundleWriter
---

# IAppxEncryptionFactory::CreateEncryptedBundleWriter


## -description

Creates a write-only bundle object to which encrypted Windows app packages can be added.

## -parameters

### -param outputStream [in]

A writable stream for writing the resulting encrypted app bundle.

### -param bundleVersion [in]

The version number of the bundle. If the bundle version is 0, a default version based on the current system time will be generated.

### -param settings [in]

Settings for creating the package.

### -param keyInfo [in]

Key info containing the base encryption key and key ID for decrypting the bundle. The base key is used to derive the per file encryption keys. If this parameter is null, the global test key and key ID are used.

### -param exemptedFiles

The list of files to be exempted from encryption.

### -param bundleWriter [out, retval]

The bundle writer object created.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxencryptionfactory">IAppxEncryptionFactory</a>
