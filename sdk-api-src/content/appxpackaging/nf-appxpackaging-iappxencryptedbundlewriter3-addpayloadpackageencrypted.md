---
UID: NF:appxpackaging.IAppxEncryptedBundleWriter3.AddPayloadPackageEncrypted
title: IAppxEncryptedBundleWriter3::AddPayloadPackageEncrypted
author: windows-sdk-content
description: Encrypts a new payload package to the bundle.
old-location: appxpkg\iappxencryptedbundlewriter3_addpayloadpackageencrypted.htm
tech.root: appxpkg
ms.assetid: DB20D7FE-BB30-4E66-9617-BDDF1E00BB6A
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: AddPayloadPackageEncrypted, AddPayloadPackageEncrypted method [App packaging and management], AddPayloadPackageEncrypted method [App packaging and management],IAppxEncryptedBundleWriter3 interface, IAppxEncryptedBundleWriter3 interface [App packaging and management],AddPayloadPackageEncrypted method, IAppxEncryptedBundleWriter3.AddPayloadPackageEncrypted, IAppxEncryptedBundleWriter3::AddPayloadPackageEncrypted, appxpackaging/IAppxEncryptedBundleWriter3::AddPayloadPackageEncrypted, appxpkg.iappxencryptedbundlewriter3_addpayloadpackageencrypted
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxEncryptedBundleWriter3.AddPayloadPackageEncrypted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxEncryptedBundleWriter3::AddPayloadPackageEncrypted


## -description


Encrypts a new payload package to the bundle.


## -parameters




### -param fileName [in]

The name of the payload file. The file name path must be relative to the root of the package.


### -param packageStream [in]

An <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> that provides the contents of <i>fileName</i>.


### -param isDefaultApplicablePackage [in]

A flag for whether this package is a default applicable package.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/20394DB5-F8E3-43E0-B222-BC14E9D6C1CB">IAppxEncryptedBundleWriter3</a>
 

 

