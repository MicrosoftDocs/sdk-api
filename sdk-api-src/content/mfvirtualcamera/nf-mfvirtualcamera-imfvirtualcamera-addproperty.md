---
UID: NF:mfvirtualcamera.IMFVirtualCamera.AddProperty
tech.root: mf
title: IMFVirtualCamera::AddProperty
ms.date: 05/17/2021
targetos: Windows
description: Adds custom device interface properties to the virtual camera. 
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: mfsensorgroup.dll
req.header: mfvirtualcamera.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: mfsensorgroup.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - mfsensorgroup.dll
api_name:
 - IMFVirtualCamera::AddProperty
f1_keywords:
 - IMFVirtualCamera::AddProperty
 - mfvirtualcamera/IMFVirtualCamera::AddProperty
dev_langs:
 - c++
---

## -description

Adds custom device interface properties to the virtual camera. 

## -parameters

### -param pKey

Pointer to a [DEVPROPKEY](/windows-hardware/drivers/install/devpropkey) to add to the virtual camera device interface. For more information, see [Unified Device Property Model](/windows-hardware/drivers/install/unified-device-property-model--windows-vista-and-later-).

### -param Type

Property type for the specified *pKey*.  The [DEVPROP_TYPE_NULL](/windows-hardware/drivers/install/devprop-type-null) and [DEVPROP_TYPE_EMPTY](/windows-hardware/drivers/install/devprop-type-empty) types are not supported.

### -param pbData

Pointer to the property data.

### -param cbData

Size in bytes contained in the buffer pointed to by *data*.

## -returns

Returns an HRESULT value, including but not limited to the following values:

| Error code | Description |
|------------|-------------|
| S_OK    | Succeeded |
| E_INVALIDARG | An input parameter is invalid. |
| E_ACCESSDENIED | Caller has insufficient permissions to add properties. |

## -remarks

Callers must have administrator-level permissions to use this API. UWP and packaged apps do not have permissions to call this method.

Callers should use caution when adding known Windows device properties as this may have unintended effects. 

## -see-also

