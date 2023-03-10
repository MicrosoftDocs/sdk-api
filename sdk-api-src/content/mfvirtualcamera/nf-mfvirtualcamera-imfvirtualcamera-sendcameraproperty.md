---
UID: NF:mfvirtualcamera.IMFVirtualCamera.SendCameraProperty
tech.root: mf
title: IMFVirtualCamera::SendCameraProperty
ms.date: 05/17/2021
targetos: Windows
description: A wrapper around the internal IKsControl::KsProperty method.
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
 - IMFVirtualCamera::SendCameraProperty
f1_keywords:
 - IMFVirtualCamera::SendCameraProperty
 - mfvirtualcamera/IMFVirtualCamera::SendCameraProperty
dev_langs:
 - c++
---

## -description

A wrapper around the internal [IKsControl::KsProperty](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty) method, which sets a property or retrieves property information, along with any other defined support operations available on a property set.

## -parameters

### -param propertySet

A GUID representing the [KSPROPERTY.Set](/windows-hardware/drivers/stream/ksmethod-structure) field.

### -param propertyId

A ULONG representing the **KSPROPERTY.Id** field.

### -param propertyFlags

A set of bit-wise or-ed flags representing the **KSPROPERTY.Flags** field.

### -param propertyPayload

Extended data added to the end of the **KSPROPERTY** structure. Any property payload provided will be added to the end of the **KSPROPERTY** structure before being sent to the virtual camera’s custom media source

### -param propertyPayloadLength

The size in bytes of the buffer pointed to by *propertyPayload*.

### -param data

The byte buffer for the payload of the property.

### -param dataLength

The size in bytes of the buffer pointed to by *data*.

### -param dataWritten

An output parameter indicating the amount of data written to the data buffer.  This value is only valid when *commandFlags* contains a GET or query operation.

## -returns

Returns an HRESULT value, including but not limited to the following values:

| Error code | Description |
|------------|-------------|
| S_OK    | Succeeded |


## -remarks


## -see-also

[IKsControl::KsProperty](/windows-hardware/drivers/ddi/ksproxy/nf-ksproxy-ikscontrol-ksproperty)

[KSPROPERTY Structure](/windows-hardware/drivers/stream/ksmethod-structure)