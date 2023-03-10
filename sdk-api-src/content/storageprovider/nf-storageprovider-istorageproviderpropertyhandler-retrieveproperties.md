---
UID: NF:storageprovider.IStorageProviderPropertyHandler.RetrieveProperties
title: IStorageProviderPropertyHandler::RetrieveProperties (storageprovider.h)
description: Gets the properties managed by the sync engine.
helpviewer_keywords: ["IStorageProviderPropertyHandler interface [Windows Shell]","RetrieveProperties method","IStorageProviderPropertyHandler.RetrieveProperties","IStorageProviderPropertyHandler::RetrieveProperties","RetrieveProperties","RetrieveProperties method [Windows Shell]","RetrieveProperties method [Windows Shell]","IStorageProviderPropertyHandler interface","shell.istorageproviderpropertyhandler_retrieveproperties","storageprovider/IStorageProviderPropertyHandler::RetrieveProperties"]
old-location: shell\istorageproviderpropertyhandler_retrieveproperties.htm
tech.root: shell
ms.assetid: C1E21E6E-A651-4AB3-A4C1-ADDF874DCCC7
ms.date: 12/05/2018
ms.keywords: IStorageProviderPropertyHandler interface [Windows Shell],RetrieveProperties method, IStorageProviderPropertyHandler.RetrieveProperties, IStorageProviderPropertyHandler::RetrieveProperties, RetrieveProperties, RetrieveProperties method [Windows Shell], RetrieveProperties method [Windows Shell],IStorageProviderPropertyHandler interface, shell.istorageproviderpropertyhandler_retrieveproperties, storageprovider/IStorageProviderPropertyHandler::RetrieveProperties
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
 - IStorageProviderPropertyHandler::RetrieveProperties
 - storageprovider/IStorageProviderPropertyHandler::RetrieveProperties
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
 - IStorageProviderPropertyHandler.RetrieveProperties
---

# IStorageProviderPropertyHandler::RetrieveProperties


## -description

Gets the properties managed by the sync engine.

## -parameters

### -param propertiesToRetrieve [in]

The identifier for the properties to retrieve.

### -param propertiesToRetrieveCount [in]

The number of properties to retrieve.

### -param retrievedProperties [out]

A collection of properties.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the file or folder cannot be found, this method should return <b>S_OK</b>, but <i>retrievedProperties</i> should be empty.

Any properties that are not managed by the sync engine should return <b>VT_EMPTY</b> for those properties.

## -see-also

<a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderpropertyhandler">IStorageProviderPropertyHandler</a>