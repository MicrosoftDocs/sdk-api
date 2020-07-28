---
UID: NF:storageprovider.IStorageProviderHandler.GetPropertyHandlerFromFileId
title: IStorageProviderHandler::GetPropertyHandlerFromFileId (storageprovider.h)
description: Gets an instance of IStorageProviderPropertyHandler associated with the provided file identifier.
helpviewer_keywords: ["GetPropertyHandlerFromFileId","GetPropertyHandlerFromFileId method [Windows Shell]","GetPropertyHandlerFromFileId method [Windows Shell]","IStorageProviderHandler interface","IStorageProviderHandler interface [Windows Shell]","GetPropertyHandlerFromFileId method","IStorageProviderHandler.GetPropertyHandlerFromFileId","IStorageProviderHandler::GetPropertyHandlerFromFileId","shell.istorageproviderhandler_getpropertyhandlerfromfileid","storageprovider/IStorageProviderHandler::GetPropertyHandlerFromFileId"]
old-location: shell\istorageproviderhandler_getpropertyhandlerfromfileid.htm
tech.root: shell
ms.assetid: 6EBC5567-E64E-47FC-A5A9-C482714401D8
ms.date: 12/05/2018
ms.keywords: GetPropertyHandlerFromFileId, GetPropertyHandlerFromFileId method [Windows Shell], GetPropertyHandlerFromFileId method [Windows Shell],IStorageProviderHandler interface, IStorageProviderHandler interface [Windows Shell],GetPropertyHandlerFromFileId method, IStorageProviderHandler.GetPropertyHandlerFromFileId, IStorageProviderHandler::GetPropertyHandlerFromFileId, shell.istorageproviderhandler_getpropertyhandlerfromfileid, storageprovider/IStorageProviderHandler::GetPropertyHandlerFromFileId
f1_keywords:
- storageprovider/IStorageProviderHandler.GetPropertyHandlerFromFileId
dev_langs:
- c++
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
- IStorageProviderHandler.GetPropertyHandlerFromFileId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStorageProviderHandler::GetPropertyHandlerFromFileId


## -description


Gets an instance of <a href="https://docs.microsoft.com/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderpropertyhandler">IStorageProviderPropertyHandler</a> associated with the provided file identifier.


## -parameters




### -param fileId [in]

The identifier for the relevant file.


### -param propertyHandler [out]

An <a href="https://docs.microsoft.com/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderpropertyhandler">IStorageProviderPropertyHandler</a> instance associated with the file specified by <i>fileId</i>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is used to convert a  file identifier to a local file system path. That path is then used to provide the <i>propertyHandler</i> to the local file.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderhandler">IStorageProviderHandler</a>
 

 

