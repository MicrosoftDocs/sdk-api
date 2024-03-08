---
UID: NF:hbaapi.HBA_RemoveCallback
tech.root: hba
title: HBA_RemoveCallback
ms.date: 08/02/2022
targetos: Windows
description: De-registers a callback routine.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: hbaapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - hbaapi.h
api_name:
 - HBA_RemoveCallback
f1_keywords:
 - HBA_RemoveCallback
 - hbaapi/HBA_RemoveCallback
dev_langs:
 - c++
helpviewer_keywords:
 - HBA_RemoveCallback
---

## -description

De-registers a callback routine.

## -parameters

### -param callbackHandle

An opaque handle (that you retrieved when you registered the callback routine) that identifies the callback routine to de-register.

## -returns

A value of type [HBA_STATUS](/windows-hardware/drivers/storage/hba-status) that indicates the status of the HBA. In particular, it returns one of the following values.

|Return code|Description|
|-|-|
|HBA_STATUS_OK|The callback routine was successfully de-registered.|
|HBA_STATUS_ERROR|An unspecified error occurred that prevented the de-registration of the callback routine.|

## -remarks

## -see-also
