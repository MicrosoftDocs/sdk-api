---
UID: NS:bluetoothapis._BLUETOOTH_DEVICE_SEARCH_PARAMS
title: "_BLUETOOTH_DEVICE_SEARCH_PARAMS"
author: windows-sdk-content
description: Specifies search criteria for Bluetooth device searches.
old-location: bluetooth\bluetooth_device_search_params.htm
old-project: bluetooth
ms.assetid: e267df61-d0f5-434f-b49c-6899c2abfa2a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: BLUETOOTH_DEVICE_SEARCH_PARAMS, BLUETOOTH_DEVICE_SEARCH_PARAMS structure [Bluetooth], _BLUETOOTH_DEVICE_SEARCH_PARAMS, bluetooth.bluetooth_device_search_params, bluetoothapis/BLUETOOTH_DEVICE_SEARCH_PARAMS
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: BLUETOOTH_DEVICE_SEARCH_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - BluetoothAPIs.h
api_name:
 - BLUETOOTH_DEVICE_SEARCH_PARAMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _BLUETOOTH_DEVICE_SEARCH_PARAMS structure


## -description


The <b>BLUETOOTH_DEVICE_SEARCH_PARAMS</b> structure specifies search criteria for Bluetooth device searches.


## -struct-fields




### -field dwSize

The size, in bytes, of the structure.


### -field fReturnAuthenticated

A value that specifies that the search should return authenticated Bluetooth devices.


### -field fReturnRemembered

A value that specifies that the search should return remembered Bluetooth devices.


### -field fReturnUnknown

A value that specifies that the search should return unknown Bluetooth devices.


### -field fReturnConnected

A value that specifies that the search should return connected Bluetooth devices.


### -field fIssueInquiry

A value that specifies that a new inquiry should be issued.


### -field cTimeoutMultiplier

A value that indicates the time out for the inquiry, expressed in increments of 1.28 seconds. For example, an inquiry of 12.8 seconds has a <b>cTimeoutMultiplier</b> value of 10. The maximum value for this member is 48. When a value greater than 48 is used, the calling function immediately fails and returns <b>E_INVALIDARG</b>.


### -field hRadio

A handle for the radio on which to perform the inquiry. Set to <b>NULL</b> to perform the inquiry on all local Bluetooth radios.


## -see-also




<a href="https://msdn.microsoft.com/cb33cf35-eb1e-4953-a779-4eb38afe0c34">BluetoothDisplayDeviceProperties</a>



<a href="https://msdn.microsoft.com/8b482d7f-56a3-47ef-be49-5272423c10f6">BluetoothFindDeviceClose</a>



<a href="https://msdn.microsoft.com/f73acbb4-119f-4a73-a338-d11e8cf7e6be">BluetoothFindFirstDevice</a>



<a href="https://msdn.microsoft.com/a17d87b2-91d7-4a03-bff7-9bc0ee48c3b4">BluetoothFindNextDevice</a>



<a href="https://msdn.microsoft.com/530e5131-a0ab-4ddd-be73-a07f94e74f73">BluetoothGetDeviceInfo</a>



<a href="https://msdn.microsoft.com/dd4f6468-ccc2-4072-95c5-97553308ae47">BluetoothRemoveDevice</a>



<a href="https://msdn.microsoft.com/afcf6708-1c2a-43ac-8e5e-1bd0ce7456fc">BluetoothUpdateDeviceRecord</a>
 

 

