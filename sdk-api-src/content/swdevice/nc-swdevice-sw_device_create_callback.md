---
UID: NC:swdevice.SW_DEVICE_CREATE_CALLBACK
title: SW_DEVICE_CREATE_CALLBACK (swdevice.h)
description: Provides a device with backing in the registry and allows the caller to then make calls to Software Device API functions with the hSwDevice handle.
helpviewer_keywords: ["SW_DEVICE_CREATE_CALLBACK","SW_DEVICE_CREATE_CALLBACK function","SW_DEVICE_CREATE_CALLBACK function pointer","swdevice.sw_device_create_callback","swdevice/SW_DEVICE_CREATE_CALLBACK"]
old-location: swdevice\sw_device_create_callback.htm
tech.root: swdevice
ms.assetid: 3955FA66-EBE2-4710-A873-C5FC8B7DBE2E
ms.date: 12/05/2018
ms.keywords: SW_DEVICE_CREATE_CALLBACK, SW_DEVICE_CREATE_CALLBACK function, SW_DEVICE_CREATE_CALLBACK function pointer, swdevice.sw_device_create_callback, swdevice/SW_DEVICE_CREATE_CALLBACK
req.header: swdevice.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
 - SW_DEVICE_CREATE_CALLBACK
 - swdevice/SW_DEVICE_CREATE_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Swdevice.h
api_name:
 - SW_DEVICE_CREATE_CALLBACK
---

# SW_DEVICE_CREATE_CALLBACK callback function


## -description

Provides a device with backing in the registry and allows the caller to then make calls to Software Device API functions with the <i>hSwDevice</i> handle.

## -parameters

### -param hSwDevice [in]

The handle for the software device.

### -param CreateResult [in]

An HRESULT that indicates if the enumeration of the software device was successful.

### -param pContext [in, optional]

The context that was optionally supplied by the client app to <a href="/windows/desktop/api/swdevice/nf-swdevice-swdevicecreate">SwDeviceCreate</a>.

### -param pszDeviceInstanceId [in, optional]

The device instance ID that PnP assigned to the device.

## -remarks

The operating system calls the <b>SW_DEVICE_CREATE_CALLBACK</b> callback function after PnP enumerates the device.  After the callback function is called, the device has backing in the registry and calls to Software Device API functions can be made by using the <i>hSwDevice</i> handle.  You can also use other APIs that work with devices for the device that is created.  

PnP enumeration of a device is the first step that a device undergoes.  After PnP enumeration of the device, the device only has registry backing, and you can set properties against the device. Just because PnP enumerated the device, the device hasn't started yet, and no driver for the device has registered or enabled interfaces yet.  In many cases, we recommend that apps wait for device-interface arrival if they want to use the device.


<div class="alert"><b>Note</b>  The callback function supplies the device instance ID for the created device. We recommend that callers of the Software Device API not try to guess at or construct the device instance ID themselves; always use the value provided by the callback function.</div>
<div> </div>
The callback function will execute on an arbitrary thread-pool thread.  Client apps can perform as much work as needed in the callback function.

In Windows 8, you can't call <a href="/windows/desktop/api/swdevice/nf-swdevice-swdeviceclose">SwDeviceClose</a> inside the callback function.  Doing so will cause a deadlock.  Be careful of releasing a ref counted object that will call <b>SwDeviceClose</b> when its destructor runs.  In Windows 8.1, this restriction is lifted, and you can call <b>SwDeviceClose</b> inside the callback function.

Always check the HRESULT that is passed to <i>CreateResult</i> to make sure PnP was able to enumerate the device.

## -see-also

<a href="/windows/desktop/api/swdevice/nf-swdevice-swdevicecreate">SwDeviceCreate</a>