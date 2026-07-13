---
UID: NF:swdevice.SwDeviceCreate
title: SwDeviceCreate function (swdevice.h)
description: Initiates the enumeration of a software device.
helpviewer_keywords: ["SwDeviceCreate","SwDeviceCreate function","swdevice.swdevicecreate","swdevice/SwDeviceCreate"]
old-location: swdevice\swdevicecreate.htm
tech.root: swdevice
ms.assetid: 8274D7D9-D4AD-412E-A9C0-7D4A08C8A14F
ms.date: 12/05/2018
ms.keywords: SwDeviceCreate, SwDeviceCreate function, swdevice.swdevicecreate, swdevice/SwDeviceCreate
req.header: swdevice.h
req.include-header: 
req.target-type: Universal
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
req.lib: Swdevice.lib; OneCoreUAP.lib on Windows 10
req.dll: Cfgmgr32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SwDeviceCreate
 - swdevice/SwDeviceCreate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cfgmgr32.dll
 - API-MS-Win-devices-swdevice-l1-1-0.dll
 - API-MS-Win-devices-swdevice-l1-1-1.dll
api_name:
 - SwDeviceCreate
---

# SwDeviceCreate function


## -description

Initiates the enumeration of a software device.

## -parameters

### -param pszEnumeratorName [in]

A string that names the enumerator of the software device.  Choose a name that represents the component that enumerates the devices.

### -param pszParentDeviceInstance [in]

A string that specifies the device instance ID of the device that is the parent of the software device.

This can be HTREE\ROOT\0, but we recommend to keep children of the root device to a minimum.  We also recommend that the preferred parent of a software device be a real device that the software device is extending the functionality for.  In situations where a software device doesn't have such a natural parent, create a device as a child of the root that can collect all the software devices that a component will enumerate; then, enumerate the actual software devices as children of this device grouping node.  This keeps the children of the root device to a manageable number.

### -param pCreateInfo [in]

A pointer to a <a href="/windows/desktop/api/swdevicedef/ns-swdevicedef-sw_device_create_info">SW_DEVICE_CREATE_INFO</a> structure that describes info that PnP uses to create the device.

### -param cPropertyCount [in]

The number of <a href="/previous-versions/windows/hardware/drivers/dn315030(v=vs.85)">DEVPROPERTY</a> structures in the <i>pProperties</i> array.

### -param pProperties [in, optional]

An optional array of <a href="/previous-versions/windows/hardware/drivers/dn315030(v=vs.85)">DEVPROPERTY</a> structures.  These properties are set on the device after it is created but before a notification that the device has been created are sent.  For more info, see Remarks.  This pointer can be <b>NULL</b>.

### -param pCallback [in]

The <a href="/windows/desktop/api/swdevice/nc-swdevice-sw_device_create_callback">SW_DEVICE_CREATE_CALLBACK</a> callback function that the operating system calls after PnP enumerates the device.

### -param pContext [in, optional]

An optional client context that the operating system passes to the callback function. This pointer can be <b>NULL</b>.

### -param phSwDevice [out]

A pointer to a variable that receives the <b>HSWDEVICE</b> handle that represents the device.  Call <a href="/windows/desktop/api/swdevice/nf-swdevice-swdeviceclose">SwDeviceClose</a> to close this handle after the client app wants PnP to remove the device.


``` syntax

DECLARE_HANDLE(HSWDEVICE);
typedef HSWDEVICE *PHSWDEVICE;

```


## -returns

S_OK is returned if device enumeration was successfully initiated.  This does not mean that the device has been successfully enumerated.  Check the <i>CreateResult</i> parameter of the <a href="/windows/desktop/api/swdevice/nc-swdevice-sw_device_create_callback">SW_DEVICE_CREATE_CALLBACK</a> callback function to determine if the device was successfully enumerated.

## -remarks

<b>SwDeviceCreate</b> returns a handle that represents the device.  After this handle is closed, PnP will remove the device.

The calling process must have Administrator access in order to initiate the enumeration of a software device.

PnP forms the device instance ID of a software device as "SWD\&lt;pszEnumeratorName&gt;\&lt;pszInstanceId&gt;," but this string might change or PnP might decorate the name.  Always get the device instance ID from the callback function.

There is a subtle difference between properties that are set as part of a <b>SwDeviceCreate</b> call and properties that are later set by calling <a href="/windows/desktop/api/swdevice/nf-swdevice-swdevicepropertyset">SwDevicePropertySet</a>.  Properties that are set as part of <b>SwDeviceCreate</b> are stored in memory; if the device is uninstalled or a null driver wipes out the property stores, these properties are written out again by the Software Device API feature when PnP re-enumerates the devices.  This is all transparent to the client.  Properties that are set using <b>SwDevicePropertySet</b> after the enumeration don't persist in memory.  But, if you set a property by using <b>SwDeviceCreate</b>, you can update the value with <b>SwDevicePropertySet</b>, and this update is applied to the in-memory value as well as the persisted store.

We recommend that all properties be specified as part of the call to <b>SwDeviceCreate</b> when possible and that these properties be specified for every call to <b>SwDeviceCreate</b>.

<div class="alert"><b>Note</b>  The operating system might possibly call <a href="/windows/desktop/api/swdevice/nc-swdevice-sw_device_create_callback">SW_DEVICE_CREATE_CALLBACK</a> before the call to <b>SwDeviceCreate</b> returns.  For this reason, the software device handle for the device is supplied as a parameter to the callback function.</div>
<div> </div>
You can create a software device as the child of a parent that is not present at the time.  PnP will enumerate the software device after the parent becomes present.

## -see-also

<a href="/windows/desktop/api/swdevice/nc-swdevice-sw_device_create_callback">SW_DEVICE_CREATE_CALLBACK</a>
