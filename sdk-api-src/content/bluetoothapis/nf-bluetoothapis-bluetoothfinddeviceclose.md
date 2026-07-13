---
UID: NF:bluetoothapis.BluetoothFindDeviceClose
title: BluetoothFindDeviceClose function (bluetoothapis.h)
description: The BluetoothFindDeviceClose function closes an enumeration handle associated with a device query.
helpviewer_keywords: ["BluetoothFindDeviceClose","BluetoothFindDeviceClose function [Bluetooth]","bluetooth.bluetoothfinddeviceclose","bluetoothapis/BluetoothFindDeviceClose"]
old-location: bluetooth\bluetoothfinddeviceclose.htm
tech.root: bluetooth
ms.assetid: 8b482d7f-56a3-47ef-be49-5272423c10f6
ms.date: 12/05/2018
ms.keywords: BluetoothFindDeviceClose, BluetoothFindDeviceClose function [Bluetooth], bluetooth.bluetoothfinddeviceclose, bluetoothapis/BluetoothFindDeviceClose
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
req.lib: Bthprops.lib
req.dll: bthprops.cpl
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BluetoothFindDeviceClose
 - bluetoothapis/BluetoothFindDeviceClose
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - bthprops.cpl
 - BluetoothAPIs.dll
 - Ext-MS-Win-Bluetooth-APIs-l1-1-0.dll
api_name:
 - BluetoothFindDeviceClose
---

# BluetoothFindDeviceClose function


## -description

The <b>BluetoothFindDeviceClose</b> function closes an enumeration handle associated with a device query.

## -parameters

### -param hFind

Handle for the query to be closed. Obtained in a previous call to the <a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindfirstdevice">BluetoothFindFirstDevice</a> function.

## -returns

Returns <b>TRUE</b> when the handle is successfully closed. Returns <b>FALSE</b> upon error. Call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function for more information on the failure.

## -see-also

<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct">BLUETOOTH_DEVICE_INFO</a>



<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_search_params">BLUETOOTH_DEVICE_SEARCH_PARAMS</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothdisplaydeviceproperties">BluetoothDisplayDeviceProperties</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindfirstdevice">BluetoothFindFirstDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindnextdevice">BluetoothFindNextDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothgetdeviceinfo">BluetoothGetDeviceInfo</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothremovedevice">BluetoothRemoveDevice</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothupdatedevicerecord">BluetoothUpdateDeviceRecord</a>