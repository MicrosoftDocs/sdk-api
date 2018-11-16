---
UID: NF:storageprovider.IStorageProviderHandler.GetPropertyHandlerFromPath
title: IStorageProviderHandler::GetPropertyHandlerFromPath
author: windows-sdk-content
description: Gets an instance of IStorageProviderPropertyHandler associated with the provided path.
old-location: shell\istorageproviderhandler_getpropertyhandlerfrompath.htm
tech.root: shell
ms.assetid: E02B43AC-73A8-4FD0-BC54-47922CA5EEDB
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetPropertyHandlerFromPath, GetPropertyHandlerFromPath method [Windows Shell], GetPropertyHandlerFromPath method [Windows Shell],IStorageProviderHandler interface, IStorageProviderHandler interface [Windows Shell],GetPropertyHandlerFromPath method, IStorageProviderHandler.GetPropertyHandlerFromPath, IStorageProviderHandler::GetPropertyHandlerFromPath, shell.istorageproviderhandler_getpropertyhandlerfrompath, storageprovider/IStorageProviderHandler::GetPropertyHandlerFromPath
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: storageprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - storageprovider.h
api_name:
 - IStorageProviderHandler.GetPropertyHandlerFromPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- storageprovider.h
: 
- IStorageProviderHandler.GetPropertyHandlerFromPath
: 
---

# IStorageProviderHandler::GetPropertyHandlerFromPath


## -description


Gets an instance of <a href="https://msdn.microsoft.com/8CB56726-DABA-44A4-ADAE-DAD8ECB047E6">IStorageProviderPropertyHandler</a> associated with the provided path.


## -parameters




### -param path [in]

The path for the relevant file.


### -param propertyHandler [out]

An <a href="https://msdn.microsoft.com/8CB56726-DABA-44A4-ADAE-DAD8ECB047E6">IStorageProviderPropertyHandler</a> instance associated with the file specified by <i>path</i>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/96DEA181-8506-4FCC-85E0-A2EF79BA6C6D">IStorageProviderHandler</a>
 

 

