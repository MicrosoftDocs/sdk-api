---
UID: NS:bluetoothapis._BLUETOOTH_SELECT_DEVICE_PARAMS
title: "_BLUETOOTH_SELECT_DEVICE_PARAMS"
author: windows-sdk-content
description: Facilitates and manages the visibility, authentication, and selection of Bluetooth devices and services.
old-location: bluetooth\bluetooth_select_device_params.htm
tech.root: Bluetooth
ms.assetid: 34ab348b-ce5d-422a-9bec-adbefa4a5ea0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BLUETOOTH_SELECT_DEVICE_PARAMS, BLUETOOTH_SELECT_DEVICE_PARAMS structure [Bluetooth], _BLUETOOTH_SELECT_DEVICE_PARAMS, _bth_bluetooth_select_device_params, bluetooth.bluetooth_select_device_params, bluetoothapis/BLUETOOTH_SELECT_DEVICE_PARAMS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - BluetoothAPIs.h
api_name:
 - BLUETOOTH_SELECT_DEVICE_PARAMS
product: Windows
targetos: Windows
req.typenames: BLUETOOTH_SELECT_DEVICE_PARAMS
req.redist: 
---

# _BLUETOOTH_SELECT_DEVICE_PARAMS structure


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

A pointer to a callback function that is called for each device. If the callback function returns <b>TRUE</b>, the item is added. If the callback function returns <b>FALSE</b>, the item is not shown. Set <b>pfnDeviceCallback</b> to null for no callback. For more information, see <a href="https://msdn.microsoft.com/8a2bf4dc-43c3-49c0-8ce0-d14ab9f4ae97">PFN_DEVICE_CALLBACK</a>.


### -field pvParam

Parameter to be passed as <b>pvParam</b> to the callback function pointed to in <b>pfnDeviceCallback</b>.


### -field cNumDevices

On input, specifies the number of desired calls. Set to zero for no limit. On output, returns the number of devices returned.


### -field pDevices

Pointer to an array of 
<a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a> structures.


## -remarks



To free the array of 
<a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a> structures passed in the <b>pDevices</b> member, call the 
<a href="https://msdn.microsoft.com/9332e62d-a7ee-452e-8e21-27bbbc82448e">BluetoothSelectDevicesFree</a> function.




## -see-also




<a href="https://msdn.microsoft.com/e80ab664-77eb-4352-ac35-64325238d4ac">BLUETOOTH_COD_PAIRS</a>



<a href="https://msdn.microsoft.com/41b14980-8217-4948-b084-1f44051d12f7">BLUETOOTH_DEVICE_INFO</a>



<a href="https://msdn.microsoft.com/97fcbd72-99d5-4c5b-bf16-75eea97cbc77">BluetoothSelectDevices</a>



<a href="https://msdn.microsoft.com/9332e62d-a7ee-452e-8e21-27bbbc82448e">BluetoothSelectDevicesFree</a>



<a href="https://msdn.microsoft.com/8a2bf4dc-43c3-49c0-8ce0-d14ab9f4ae97">PFN_DEVICE_CALLBACK</a>
 

 

