---
UID: NS:bluetoothapis._BLUETOOTH_COD_PAIRS
title: BLUETOOTH_COD_PAIRS (bluetoothapis.h)
description: The BLUETOOTH_COD_PAIRS structure provides for specification and retrieval of Bluetooth Class Of Device (COD) information.
helpviewer_keywords: ["BLUETOOTH_COD_PAIRS","BLUETOOTH_COD_PAIRS structure [Bluetooth]","_bth_bluetooth_cod_pairs","bluetooth.bluetooth_cod_pairs","bluetoothapis/BLUETOOTH_COD_PAIRS"]
old-location: bluetooth\bluetooth_cod_pairs.htm
tech.root: bluetooth
ms.assetid: e80ab664-77eb-4352-ac35-64325238d4ac
ms.date: 12/05/2018
ms.keywords: BLUETOOTH_COD_PAIRS, BLUETOOTH_COD_PAIRS structure [Bluetooth], _bth_bluetooth_cod_pairs, bluetooth.bluetooth_cod_pairs, bluetoothapis/BLUETOOTH_COD_PAIRS
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
req.typenames: BLUETOOTH_COD_PAIRS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BLUETOOTH_COD_PAIRS
 - bluetoothapis/_BLUETOOTH_COD_PAIRS
 - BLUETOOTH_COD_PAIRS
 - bluetoothapis/BLUETOOTH_COD_PAIRS
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
 - BLUETOOTH_COD_PAIRS
---

# BLUETOOTH_COD_PAIRS structure


## -description

The 
<b>BLUETOOTH_COD_PAIRS</b> structure provides for specification and retrieval of Bluetooth Class Of Device (COD) information.

## -struct-fields

### -field ulCODMask

A mask to compare to determine the class of device. The major and minor codes of <b>ulCODMask</b> are used to compare  the class of device found.  If a major code is provided  it must match the major code returned by the remote device, such that GET_COD_MAJOR(ulCODMask) is equal to GET_COD_MAJOR([class of device of the remote device]).

### -field pcszDescription

Descriptive string of the mask.

## -remarks

If a minor code is provided in <b>ulCODMask</b> it must also match the minor code returned by the remote device.  A major code must be set if a minor code is specified; zero is not a valid major code.

See the Bluetooth specification at 
<a href="https://www.bluetooth.com/">www.bluetooth.com</a> for Class Of Device information.

## -see-also

<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_select_device_params">BLUETOOTH_SELECT_DEVICE_PARAMS </a>

