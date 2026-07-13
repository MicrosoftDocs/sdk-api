---
UID: NF:storageprovider.IStorageProviderPropertyHandler.SaveProperties
title: IStorageProviderPropertyHandler::SaveProperties (storageprovider.h)
description: Saves properties associated with a file or folder.
helpviewer_keywords: ["IStorageProviderPropertyHandler interface [Windows Shell]","SaveProperties method","IStorageProviderPropertyHandler.SaveProperties","IStorageProviderPropertyHandler::SaveProperties","SaveProperties","SaveProperties method [Windows Shell]","SaveProperties method [Windows Shell]","IStorageProviderPropertyHandler interface","shell.istorageproviderpropertyhandler_saveproperties","storageprovider/IStorageProviderPropertyHandler::SaveProperties"]
old-location: shell\istorageproviderpropertyhandler_saveproperties.htm
tech.root: shell
ms.assetid: 983751BA-BF36-4018-A95A-4BEA1E9BA3BF
ms.date: 12/05/2018
ms.keywords: IStorageProviderPropertyHandler interface [Windows Shell],SaveProperties method, IStorageProviderPropertyHandler.SaveProperties, IStorageProviderPropertyHandler::SaveProperties, SaveProperties, SaveProperties method [Windows Shell], SaveProperties method [Windows Shell],IStorageProviderPropertyHandler interface, shell.istorageproviderpropertyhandler_saveproperties, storageprovider/IStorageProviderPropertyHandler::SaveProperties
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
 - IStorageProviderPropertyHandler::SaveProperties
 - storageprovider/IStorageProviderPropertyHandler::SaveProperties
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
 - IStorageProviderPropertyHandler.SaveProperties
---

# IStorageProviderPropertyHandler::SaveProperties


## -description

Saves properties associated with a file or folder.

## -parameters

### -param propertiesToSave [in]

The properties to save.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Attempting to save properties that are not managed by the sync engine should result in the error code <b>E_INVALIDARG</b>.

## -see-also

<a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderpropertyhandler">IStorageProviderPropertyHandler</a>