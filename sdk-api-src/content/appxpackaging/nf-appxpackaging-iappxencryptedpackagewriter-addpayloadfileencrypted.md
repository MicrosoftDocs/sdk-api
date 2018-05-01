---
UID: NF:appxpackaging.IAppxEncryptedPackageWriter.AddPayloadFileEncrypted
title: IAppxEncryptedPackageWriter::AddPayloadFileEncrypted method
author: windows-driver-content
description: Adds a new encrypted payload file to the appx package.
old-location: appxpkg\iappxencryptedpackagewriter_addpayloadfileencrypted.htm
old-project: appxpkg
ms.assetid: 4F5823D3-7039-4CA1-BEEA-DF2A13BC54BD
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: AddPayloadFileEncrypted method [App packaging and management], AddPayloadFileEncrypted method [App packaging and management], IAppxEncryptedPackageWriter interface, AddPayloadFileEncrypted,IAppxEncryptedPackageWriter.AddPayloadFileEncrypted, IAppxEncryptedPackageWriter, IAppxEncryptedPackageWriter interface [App packaging and management], AddPayloadFileEncrypted method, IAppxEncryptedPackageWriter::AddPayloadFileEncrypted, appxpackaging/IAppxEncryptedPackageWriter::AddPayloadFileEncrypted, appxpkg.iappxencryptedpackagewriter_addpayloadfileencrypted
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: APPX_PACKAGE_EDITOR_UPDATE_PACKAGE_OPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	AppxPackaging.h
api_name:
-	IAppxEncryptedPackageWriter.AddPayloadFileEncrypted
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAppxEncryptedPackageWriter::AddPayloadFileEncrypted method


## -description


Adds a new encrypted payload file to the appx package.


## -parameters




### -param fileName [in]

The name of the payload file. The file name path must be relative to the root of the package.


### -param compressionOption [in]


            The type of compression to use  to store <i>fileName</i> in the package. 


### -param inputStream [in]


            An <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> providing the contents of <i>fileName</i>.
          The stream must support <a href="https://msdn.microsoft.com/library/windows/hardware/hh439702">Read</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/hh439723">Seek</a>, and <a href="https://msdn.microsoft.com/c22ab396-dbc5-43a0-8448-35a2c094464f">Stat</a>.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/19096DFB-A8CF-4DEF-863B-3DBB9E893A8D">IAppxEncryptedPackageWriter</a>
 

 

