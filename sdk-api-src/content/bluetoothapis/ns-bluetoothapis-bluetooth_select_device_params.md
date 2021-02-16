---
UID: NS:bluetoothapis._BLUETOOTH_SELECT_DEVICE_PARAMS
title: BLUETOOTH_SELECT_DEVICE_PARAMS (bluetoothapis.h)
description: Facilitates and manages the visibility, authentication, and selection of Bluetooth devices and services.
helpviewer_keywords: ["BLUETOOTH_SELECT_DEVICE_PARAMS","BLUETOOTH_SELECT_DEVICE_PARAMS structure [Bluetooth]","_bth_bluetooth_select_device_params","bluetooth.bluetooth_select_device_params","bluetoothapis/BLUETOOTH_SELECT_DEVICE_PARAMS"]
old-location: bluetooth\bluetooth_select_device_params.htm
tech.root: bluetooth
ms.assetid: 34ab348b-ce5d-422a-9bec-adbefa4a5ea0
ms.date: 12/05/2018
ms.keywords: BLUETOOTH_SELECT_DEVICE_PARAMS, BLUETOOTH_SELECT_DEVICE_PARAMS structure [Bluetooth], _bth_bluetooth_select_device_params, bluetooth.bluetooth_select_device_params, bluetoothapis/BLUETOOTH_SELECT_DEVICE_PARAMS
req.header: bluetoothapis.h
req.include-header: Bthsdpdef.h, BluetoothAPIs.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: BLUETOOTH_SELECT_DEVICE_PARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BLUETOOTH_SELECT_DEVICE_PARAMS
 - bluetoothapis/_BLUETOOTH_SELECT_DEVICE_PARAMS
 - BLUETOOTH_SELECT_DEVICE_PARAMS
 - bluetoothapis/BLUETOOTH_SELECT_DEVICE_PARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - BluetoothAPIs.h
api_name:
 - BLUETOOTH_SELECT_DEVICE_PARAMS
---

# BLUETOOTH_SELECT_DEVICE_PARAMS structure


## -description

The 
<b>BLUETOOTH_SELECT_DEVICE_PARAMS</b> structure facilitates and manages the visibility, authentication, and selection of Bluetooth devices and services.

## -struct-fields

### -field dwSize

Size, in bytes, of the 
<b>BLUETOOTH_SELECT_DEVICE_PARAMS</b> structure.

### -field cNumOfClasses

Number of classes in <b>prgClassOfDevices</b>. Set to zero to search for all devices.

### -field prgClassOfDevices

Array of class of devices to find.

### -field pszInfo

Sets the information text when not <b>NULL</b>.

### -field hwndParent

Handle to the parent window. Set to <b>NULL</b> for no parent.

### -field fForceAuthentication

If <b>TRUE</b>, forces authentication before returning.

### -field fShowAuthenticated

If <b>TRUE</b>, authenticated devices are shown in the picker.

### -field fShowRemembered

If <b>TRUE</b>, remembered devices are shown in the picker.

### -field fShowUnknown

If <b>TRUE</b>, unknown devices that are not authenticated or remembered are shown in the picker.

### -field fAddNewDeviceWizard

If <b>TRUE</b>, starts the Add New Device wizard.

### -field fSkipServicesPage

If <b>TRUE</b>, skips the Services page in the Add New Device wizard.

### -field pfnDeviceCallback

A pointer to a callback function that is called for each device. If the callback function returns <b>TRUE</b>, the item is added. If the callback function returns <b>FALSE</b>, the item is not shown. Set <b>pfnDeviceCallback</b> to null for no callback. For more information, see <a href="/windows/desktop/api/bluetoothapis/nc-bluetoothapis-pfn_device_callback">PFN_DEVICE_CALLBACK</a>.

### -field pvParam

Parameter to be passed as <b>pvParam</b> to the callback function pointed to in <b>pfnDeviceCallback</b>.

### -field cNumDevices

On input, specifies the number of desired calls. Set to zero for no limit. On output, returns the number of devices returned.

### -field pDevices

Pointer to an array of 
<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a> structures.

## -remarks

To free the array of 
<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a> structures passed in the <b>pDevices</b> member, call the 
<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothselectdevicesfree">BluetoothSelectDevicesFree</a> function.

## -see-also

<a href="/windows/desktop/api/bluetoothapis/ns-bluetoothapis-bluetooth_cod_pairs">BLUETOOTH_COD_PAIRS</a>



<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothselectdevices">BluetoothSelectDevices</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothselectdevicesfree">BluetoothSelectDevicesFree</a>



<a href="/windows/desktop/api/bluetoothapis/nc-bluetoothapis-pfn_device_callback">PFN_DEVICE_CALLBACK</a>