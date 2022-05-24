---
UID: NF:deliveryoptimization.IDODownload.GetProperty
tech.root: delivery_optimization
title: IDODownload::GetProperty
ms.date: 05/04/2022
targetos: Windows
description: Retrieves a pointer to a **VARIANT** that contains a specific download property.
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
 - IDODownload::GetProperty
f1_keywords:
 - IDODownload::GetProperty
 - deliveryoptimization/IDODownload::GetProperty
dev_langs:
 - c++
helpviewer_keywords:
 - GetProperty
prerelease: false
---

## -description

Retrieves a pointer to a **VARIANT** that contains a specific download property.

## -parameters

### -param propId

The required property ID to get (of type **DODownloadProperty**).

### -param propVal

The resulting property value, stored in a **VARIANT**.

## -returns

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).

|Return value|Description|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propId* is unknown.|
|DO_E_WRITE_ONLY_PROPERTY|The property is write-only, and can't be read.|
|E_NOT_SET|No such property was set via **SetProperty**.|

## -remarks

## -see-also
