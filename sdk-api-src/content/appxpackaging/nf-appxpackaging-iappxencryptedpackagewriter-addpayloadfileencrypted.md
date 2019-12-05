---
UID: NF:appxpackaging.IAppxEncryptedPackageWriter.AddPayloadFileEncrypted
title: IAppxEncryptedPackageWriter::AddPayloadFileEncrypted (appxpackaging.h)
description: Adds a new encrypted payload file to the appx package.
old-location: appxpkg\iappxencryptedpackagewriter_addpayloadfileencrypted.htm
tech.root: appxpkg
ms.assetid: 4F5823D3-7039-4CA1-BEEA-DF2A13BC54BD
ms.date: 12/05/2018
ms.keywords: AddPayloadFileEncrypted, AddPayloadFileEncrypted method [App packaging and management], AddPayloadFileEncrypted method [App packaging and management],IAppxEncryptedPackageWriter interface, IAppxEncryptedPackageWriter interface [App packaging and management],AddPayloadFileEncrypted method, IAppxEncryptedPackageWriter.AddPayloadFileEncrypted, IAppxEncryptedPackageWriter::AddPayloadFileEncrypted, appxpackaging/IAppxEncryptedPackageWriter::AddPayloadFileEncrypted, appxpkg.iappxencryptedpackagewriter_addpayloadfileencrypted
ms.topic: method
f1_keywords:
- appxpackaging/IAppxEncryptedPackageWriter.AddPayloadFileEncrypted
dev_langs:
- c++
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
- IAppxEncryptedPackageWriter.AddPayloadFileEncrypted
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAppxEncryptedPackageWriter::AddPayloadFileEncrypted


## -description


Adds a new encrypted payload file to the appx package.


## -parameters




### -param fileName [in]

The name of the payload file. The file name path must be relative to the root of the package.


### -param compressionOption [in]

The type of compression to use  to store <i>fileName</i> in the package. 


### -param inputStream [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> providing the contents of <i>fileName</i>.
          The stream must support <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">Read</a>, <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-seek">Seek</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-stat">Stat</a>.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxencryptedpackagewriter">IAppxEncryptedPackageWriter</a>
 

 

