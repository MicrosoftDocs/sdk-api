---
UID: NF:storageprovider.IStorageProviderPropertyHandler.RetrieveProperties
title: IStorageProviderPropertyHandler::RetrieveProperties
author: windows-driver-content
description: Gets the properties managed by the sync engine.
old-location: shell\istorageproviderpropertyhandler_retrieveproperties.htm
old-project: shell
ms.assetid: C1E21E6E-A651-4AB3-A4C1-ADDF874DCCC7
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IStorageProviderPropertyHandler interface [Windows Shell],RetrieveProperties method, IStorageProviderPropertyHandler.RetrieveProperties, IStorageProviderPropertyHandler::RetrieveProperties, RetrieveProperties, RetrieveProperties method [Windows Shell], RetrieveProperties method [Windows Shell],IStorageProviderPropertyHandler interface, shell.istorageproviderpropertyhandler_retrieveproperties, storageprovider/IStorageProviderPropertyHandler::RetrieveProperties
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
-	IStorageProviderPropertyHandler.RetrieveProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IStorageProviderPropertyHandler::RetrieveProperties


## -description


Gets the properties managed by the sync engine.


## -parameters




### -param propertiesToRetrieve [in]

The identifier for the properties to retrieve.


### -param propertiesToRetrieveCount [in]

The number of properties to retrieve.


### -param retrievedProperties






#### - **retrievedProperties [out]

A collection of properties.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the file or folder cannot be found, this method should return <b>S_OK</b>, but <i>retrievedProperties</i> should be empty.

Any properties that are not managed by the sync engine should return <b>VT_EMPTY</b> for those properties.




## -see-also




<a href="https://msdn.microsoft.com/8CB56726-DABA-44A4-ADAE-DAD8ECB047E6">IStorageProviderPropertyHandler</a>
 

 

