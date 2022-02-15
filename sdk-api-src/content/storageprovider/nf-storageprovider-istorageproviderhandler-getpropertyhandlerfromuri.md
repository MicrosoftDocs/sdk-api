---
UID: NF:storageprovider.IStorageProviderHandler.GetPropertyHandlerFromUri
title: IStorageProviderHandler::GetPropertyHandlerFromUri (storageprovider.h)
description: Gets an instance of IStorageProviderPropertyHandler associated with the provided URI.
helpviewer_keywords: ["GetPropertyHandlerFromUri","GetPropertyHandlerFromUri method [Windows Shell]","GetPropertyHandlerFromUri method [Windows Shell]","IStorageProviderHandler interface","IStorageProviderHandler interface [Windows Shell]","GetPropertyHandlerFromUri method","IStorageProviderHandler.GetPropertyHandlerFromUri","IStorageProviderHandler::GetPropertyHandlerFromUri","shell.istorageproviderhandler_getpropertyhandlerfromuri","storageprovider/IStorageProviderHandler::GetPropertyHandlerFromUri"]
old-location: shell\istorageproviderhandler_getpropertyhandlerfromuri.htm
tech.root: shell
ms.assetid: C02A9690-1E98-4960-B5E7-E75BDAAF9A62
ms.date: 12/05/2018
ms.keywords: GetPropertyHandlerFromUri, GetPropertyHandlerFromUri method [Windows Shell], GetPropertyHandlerFromUri method [Windows Shell],IStorageProviderHandler interface, IStorageProviderHandler interface [Windows Shell],GetPropertyHandlerFromUri method, IStorageProviderHandler.GetPropertyHandlerFromUri, IStorageProviderHandler::GetPropertyHandlerFromUri, shell.istorageproviderhandler_getpropertyhandlerfromuri, storageprovider/IStorageProviderHandler::GetPropertyHandlerFromUri
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStorageProviderHandler::GetPropertyHandlerFromUri
 - storageprovider/IStorageProviderHandler::GetPropertyHandlerFromUri
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - storageprovider.h
api_name:
 - IStorageProviderHandler.GetPropertyHandlerFromUri
---

# IStorageProviderHandler::GetPropertyHandlerFromUri


## -description

Gets an instance of <a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderpropertyhandler">IStorageProviderPropertyHandler</a> associated with the provided URI.

## -parameters

### -param uri [in]

The URI for the relevant file.

### -param propertyHandler [out]

An <a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderpropertyhandler">IStorageProviderPropertyHandler</a> instance associated with the file specified by <i>uri</i>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is used to convert a remote URI to a local file system path. That path is then used to provide the <i>propertyHandler</i> to the local file.

## -see-also

<a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderhandler">IStorageProviderHandler</a>