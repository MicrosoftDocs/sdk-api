---
UID: NF:appxpackaging.IAppxEncryptedPackageWriter2.AddPayloadFilesEncrypted
title: IAppxEncryptedPackageWriter2::AddPayloadFilesEncrypted (appxpackaging.h)
author: windows-sdk-content
description: Adds one or more payload files to an encrypted app package.
old-location: appxpkg\iappxencryptedpackagewriter2_addpayloadfilesencrypted.htm
tech.root: appxpkg
ms.assetid: 3C304E54-B4BA-4A9E-B774-1DA119A09C07
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddPayloadFilesEncrypted, AddPayloadFilesEncrypted method [App packaging and management], AddPayloadFilesEncrypted method [App packaging and management],IAppxEncryptedPackageWriter2 interface, IAppxEncryptedPackageWriter2 interface [App packaging and management],AddPayloadFilesEncrypted method, IAppxEncryptedPackageWriter2.AddPayloadFilesEncrypted, IAppxEncryptedPackageWriter2::AddPayloadFilesEncrypted, appxpackaging/IAppxEncryptedPackageWriter2::AddPayloadFilesEncrypted, appxpkg.iappxencryptedpackagewriter2_addpayloadfilesencrypted
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
 - IAppxEncryptedPackageWriter2.AddPayloadFilesEncrypted
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAppxEncryptedPackageWriter2::AddPayloadFilesEncrypted


## -description


Adds one or more payload files to an encrypted app package.


## -parameters




### -param fileCount [in]

The number of payload files to be added to the encrypted app package.


### -param payloadFiles [in]

The payload files to be added.


### -param memoryLimit [in]

The memory limit in bytes.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/C45364CE-9943-4677-856D-8761CF21EB36">IAppxEncryptedPackageWriter2</a>
 

 

