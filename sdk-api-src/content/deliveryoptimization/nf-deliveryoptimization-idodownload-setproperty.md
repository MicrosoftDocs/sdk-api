---
UID: NF:deliveryoptimization.IDODownload.SetProperty
tech.root: delivery_optimization
title: IDODownload::SetProperty
ms.date: 05/04/2022
targetos: Windows
description: Sets a download property.
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
 - IDODownload::SetProperty
f1_keywords:
 - IDODownload::SetProperty
 - deliveryoptimization/IDODownload::SetProperty
dev_langs:
 - c++
helpviewer_keywords:
 - SetProperty
prerelease: false
---

## -description

Sets a download property. The method accepts a pointer to a **VARIANT** that contains a specific property to apply to the download.

## -parameters

### -param propId

The required property ID to set (of type **DODownloadProperty**).

### -param propVal

The property value to set, stored in a **VARIANT**.

## -returns

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

|Return value|Description|
|-|-|
|DO_E_UNKNOWN_PROPERTY_ID|*propId* is unknown.|
|DO_E_INVALID_STATE|The download is not currently in a state that allows setting properties.|

## -remarks

## -see-also
