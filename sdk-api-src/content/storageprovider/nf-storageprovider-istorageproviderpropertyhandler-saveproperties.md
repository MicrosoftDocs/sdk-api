---
UID: NF:storageprovider.IStorageProviderPropertyHandler.SaveProperties
title: IStorageProviderPropertyHandler::SaveProperties
author: windows-sdk-content
description: Saves properties associated with a file or folder.
old-location: shell\istorageproviderpropertyhandler_saveproperties.htm
tech.root: shell
ms.assetid: 983751BA-BF36-4018-A95A-4BEA1E9BA3BF
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IStorageProviderPropertyHandler interface [Windows Shell],SaveProperties method, IStorageProviderPropertyHandler.SaveProperties, IStorageProviderPropertyHandler::SaveProperties, SaveProperties, SaveProperties method [Windows Shell], SaveProperties method [Windows Shell],IStorageProviderPropertyHandler interface, shell.istorageproviderpropertyhandler_saveproperties, storageprovider/IStorageProviderPropertyHandler::SaveProperties
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
 - IStorageProviderPropertyHandler.SaveProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStorageProviderPropertyHandler::SaveProperties


## -description


Saves properties associated with a file or folder.


## -parameters




### -param propertiesToSave

TBD




#### - *propertiesToSave [in]

The properties to save.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Attempting to save properties that are not managed by the sync engine should result in the error code <b>E_INVALIDARG</b>.




## -see-also




<a href="https://msdn.microsoft.com/8CB56726-DABA-44A4-ADAE-DAD8ECB047E6">IStorageProviderPropertyHandler</a>
 

 

