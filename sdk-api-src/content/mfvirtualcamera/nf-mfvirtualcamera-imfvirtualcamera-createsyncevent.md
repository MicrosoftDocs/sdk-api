---
UID: NF:mfvirtualcamera.IMFVirtualCamera.CreateSyncEvent
tech.root: mf
title: IMFVirtualCamera::CreateSyncEvent
ms.date: 05/17/2021
targetos: Windows
description: A wrapper around the IKsControl::KsEvent method, which enables or disables an event.
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
 - IMFVirtualCamera::CreateSyncEvent
f1_keywords:
 - IMFVirtualCamera::CreateSyncEvent
 - mfvirtualcamera/IMFVirtualCamera::CreateSyncEvent
dev_langs:
 - c++
---

## -description

A wrapper around the [IKsControl::KsEvent](/windows-hardware/drivers/ddi/ks/nf-ks-ikscontrol-ksevent) method, which enables or disables an event.

## -parameters

### -param kseventSet

A GUID representing the [KSEVENT.Set](/previous-versions/ff561744(v=vs.85)) field.

### -param kseventId

A ULONG representing the **KSEVENT.Id** field.

### -param kseventFlags

A set of bit-wise or-ed flags representing the **KSEVENT.Flags** field.

### -param eventHandle

A Handle representing the [KSEVENTDATA.EventHandle.Event](/windows-hardware/drivers/ddi/ks/ns-ks-kseventdata) field.

### -param cameraSyncObject

An output parameter that receives an [IMFSyncObject](nn-mfvirtualcamera-imfcamerasyncobject.md) interface.  The caller is responsible for releasing this object.

## -returns

Returns an HRESULT value, including but not limited to the following values:

| Error code | Description |
|------------|-------------|
| S_OK    | Succeeded |

## -remarks

This method allows the caller to create a event object between the caller and the virtual camera for synchronization.  The virtual camera implementation will receive a call to **IKsControl::KsEvent** when this API is called. The resulting [IMFCameraSyncObject](nn-mfvirtualcamera-imfcamerasyncobject.md) can be used to block on the event from the virtual camera.


When the **IMFCameraSyncObject** is obtained, the caller may choose to use the [IMFCameraSyncObject::WaitOnSignal](nf-mfvirtualcamera-imfcamerasyncobject-waitonsignal.md) method or call [WaitForSingleObject](../synchapi/nf-synchapi-waitforsingleobject.md) or [WaitForMultipleObjects](../synchapi/nf-synchapi-waitformultipleobjects.md) on the HANDLE that was provided to the **CreateSyncObject** method.  The caller must not wait on both, as the signal on the event may only be set once by the driver.

The caller must call [IMFCameraSyncObject::Shutdown](nf-mfvirtualcamera-imfvirtualcamera-shutdown.md) when the synchronization object is no longer needed regardless of whether the wait operation succeeded or not.


## -see-also

[IKsControl::KsEvent](/windows-hardware/drivers/ddi/ks/nf-ks-ikscontrol-ksevent)

[IMFCameraSyncObject](nn-mfvirtualcamera-imfcamerasyncobject.md)

[IMFCameraSyncObject::WaitOnSignal](nf-mfvirtualcamera-imfcamerasyncobject-waitonsignal.md)

[WaitForSingleObject](../synchapi/nf-synchapi-waitforsingleobject.md)

[WaitForMultipleObjects](../synchapi/nf-synchapi-waitformultipleobjects.md)

