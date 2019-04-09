---
UID: NF:appxpackaging.IAppxEncryptedBundleWriter.AddPayloadPackageEncrypted
title: IAppxEncryptedBundleWriter::AddPayloadPackageEncrypted (appxpackaging.h)
author: windows-sdk-content
description: Encrypts a new payload package to the bundle.
old-location: appxpkg\iappxencryptedbundlewriter_addpayloadpackageencrypted.htm
tech.root: appxpkg
ms.assetid: 974C29A7-3FEE-4042-986F-D8FD3774F9A6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddPayloadPackageEncrypted, AddPayloadPackageEncrypted method [App packaging and management], AddPayloadPackageEncrypted method [App packaging and management],IAppxEncryptedBundleWriter interface, IAppxEncryptedBundleWriter interface [App packaging and management],AddPayloadPackageEncrypted method, IAppxEncryptedBundleWriter.AddPayloadPackageEncrypted, IAppxEncryptedBundleWriter::AddPayloadPackageEncrypted, appxpackaging/IAppxEncryptedBundleWriter::AddPayloadPackageEncrypted, appxpkg.iappxencryptedbundlewriter_addpayloadpackageencrypted
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxEncryptedBundleWriter.AddPayloadPackageEncrypted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxEncryptedBundleWriter::AddPayloadPackageEncrypted


## -description


Encrypts a new payload package to the bundle.


## -parameters




### -param fileName [in]

The name of the payload file. The file name path must be relative to the root of the package.


### -param packageStream [in]

An <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> that provides the contents of <i>fileName</i>.
          The stream must support <a href="https://msdn.microsoft.com/934a90bb-5ed0-4d80-9906-352ad8586655">Read</a>, <a href="https://msdn.microsoft.com/ea087c6d-8854-4a81-b37b-15ab76630973">Seek</a>, and <a href="https://msdn.microsoft.com/c22ab396-dbc5-43a0-8448-35a2c094464f">Stat</a>.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/E88355DA-F7BE-45C7-9DDB-EC39DB2AD280">IAppxEncryptedBundleWriter</a>
 

 

