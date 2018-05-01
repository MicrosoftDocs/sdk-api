---
UID: NF:storageprovider.IStorageProviderHandler.GetPropertyHandlerFromUri
title: IStorageProviderHandler::GetPropertyHandlerFromUri method
author: windows-driver-content
description: Gets an instance of IStorageProviderPropertyHandler associated with the provided URI.
old-location: shell\istorageproviderhandler_getpropertyhandlerfromuri.htm
old-project: shell
ms.assetid: C02A9690-1E98-4960-B5E7-E75BDAAF9A62
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetPropertyHandlerFromUri method [Windows Shell], GetPropertyHandlerFromUri method [Windows Shell], IStorageProviderHandler interface, GetPropertyHandlerFromUri,IStorageProviderHandler.GetPropertyHandlerFromUri, IStorageProviderHandler, IStorageProviderHandler interface [Windows Shell], GetPropertyHandlerFromUri method, IStorageProviderHandler::GetPropertyHandlerFromUri, shell.istorageproviderhandler_getpropertyhandlerfromuri, storageprovider/IStorageProviderHandler::GetPropertyHandlerFromUri
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
req.typenames: MPR50_SERVICE_CHARACTERISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	storageprovider.h
api_name:
-	IStorageProviderHandler.GetPropertyHandlerFromUri
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IStorageProviderHandler::GetPropertyHandlerFromUri method


## -description


Gets an instance of <a href="https://msdn.microsoft.com/8CB56726-DABA-44A4-ADAE-DAD8ECB047E6">IStorageProviderPropertyHandler</a> associated with the provided URI.


## -parameters




### -param uri [in]

The URI for the relevant file.


### -param propertyHandler






#### - **propertyHandler [out]

An <a href="https://msdn.microsoft.com/8CB56726-DABA-44A4-ADAE-DAD8ECB047E6">IStorageProviderPropertyHandler</a> instance associated with the file specified by <i>uri</i>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is used to convert a remote URI to a local file system path. That path is then used to provide the <i>propertyHandler</i> to the local file.




## -see-also




<a href="https://msdn.microsoft.com/96DEA181-8506-4FCC-85E0-A2EF79BA6C6D">IStorageProviderHandler</a>
 

 

