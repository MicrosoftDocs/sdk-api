---
UID: NF:appxpackaging.IAppxEncryptionFactory3.CreateEncryptedBundleWriter
title: IAppxEncryptionFactory3::CreateEncryptedBundleWriter (appxpackaging.h)
description: Creates a write-only bundle object to which encrypted Windows app packages can be added. (IAppxEncryptionFactory3.CreateEncryptedBundleWriter)
helpviewer_keywords: ["CreateEncryptedBundleWriter","CreateEncryptedBundleWriter method [App packaging and management]","CreateEncryptedBundleWriter method [App packaging and management]","IAppxEncryptionFactory3 interface","IAppxEncryptionFactory3 interface [App packaging and management]","CreateEncryptedBundleWriter method","IAppxEncryptionFactory3.CreateEncryptedBundleWriter","IAppxEncryptionFactory3::CreateEncryptedBundleWriter","appxpackaging/IAppxEncryptionFactory3::CreateEncryptedBundleWriter","appxpkg.iappxencryptionfactory3_createencryptedbundlewriter"]
old-location: appxpkg\iappxencryptionfactory3_createencryptedbundlewriter.htm
tech.root: appxpkg
ms.assetid: 6E12E38B-23F3-437A-B3DF-1614663CFD3F
ms.date: 12/05/2018
ms.keywords: CreateEncryptedBundleWriter, CreateEncryptedBundleWriter method [App packaging and management], CreateEncryptedBundleWriter method [App packaging and management],IAppxEncryptionFactory3 interface, IAppxEncryptionFactory3 interface [App packaging and management],CreateEncryptedBundleWriter method, IAppxEncryptionFactory3.CreateEncryptedBundleWriter, IAppxEncryptionFactory3::CreateEncryptedBundleWriter, appxpackaging/IAppxEncryptionFactory3::CreateEncryptedBundleWriter, appxpkg.iappxencryptionfactory3_createencryptedbundlewriter
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
 - IAppxEncryptionFactory3::CreateEncryptedBundleWriter
 - appxpackaging/IAppxEncryptionFactory3::CreateEncryptedBundleWriter
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
 - IAppxEncryptionFactory3.CreateEncryptedBundleWriter
---

# IAppxEncryptionFactory3::CreateEncryptedBundleWriter


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

### -param exemptedFiles [in]

Files exempted from the bundle writer.

### -param bundleWriter [out, retval]

The bundle writer object created.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxencryptionfactory3">IAppxEncryptionFactory3</a>
