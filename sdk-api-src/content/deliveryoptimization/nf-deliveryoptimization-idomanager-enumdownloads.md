---
UID: NF:deliveryoptimization.IDOManager.EnumDownloads
tech.root: delivery_optimization
title: IDOManager::EnumDownloads
ms.date: 05/04/2022
targetos: Windows
description: Retrieves an interface pointer to an enumerator object that is used to enumerate existing downloads.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: deliveryoptimization.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 Build 22621
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - deliveryoptimization.h
api_name:
 - IDOManager::EnumDownloads
f1_keywords:
 - IDOManager::EnumDownloads
 - deliveryoptimization/IDOManager::EnumDownloads
dev_langs:
 - c++
helpviewer_keywords:
 - EnumDownloads
prerelease: false
---

## -description

Retrieves an interface pointer to an enumerator object that is used to enumerate existing downloads.

## -parameters

### -param category

Optional. The property name to be used as a category to enumerate. Passing `nullptr` will retrieve all existing downloads. The following properties are supported as a category.

- **DODownloadProperty_Id**
- **DODownloadProperty_Uri**
- **DODownloadProperty_ContentId**
- **DODownloadProperty_DisplayName**
- **DODownloadProperty_LocalPath**

### -param ppEnum

The address of an interface pointer to **IEnumUnknown**, which is used to enumerate existing downloads. The contents of the enumerator depend on the value of *category*. The downloads included in the enumeration interface are the ones that were previously created by the same caller to this function.

## -returns

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also
