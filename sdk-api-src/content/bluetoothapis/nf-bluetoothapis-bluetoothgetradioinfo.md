---
UID: NF:bluetoothapis.BluetoothGetRadioInfo
title: BluetoothGetRadioInfo function (bluetoothapis.h)
description: Obtains information about a Bluetooth radio.
helpviewer_keywords: ["BluetoothGetRadioInfo","BluetoothGetRadioInfo function [Bluetooth]","bluetooth.bluetoothgetradioinfo","bluetoothapis/BluetoothGetRadioInfo"]
old-location: bluetooth\bluetoothgetradioinfo.htm
tech.root: bluetooth
ms.assetid: 0c596f49-70f9-4a58-842c-e01dcf69bd01
ms.date: 12/05/2018
ms.keywords: BluetoothGetRadioInfo, BluetoothGetRadioInfo function [Bluetooth], bluetooth.bluetoothgetradioinfo, bluetoothapis/BluetoothGetRadioInfo
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
 - BluetoothGetRadioInfo
 - bluetoothapis/BluetoothGetRadioInfo
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
 - BluetoothGetRadioInfo
---

# BluetoothGetRadioInfo function


## -description

The <b>BluetoothGetRadioInfo</b> function obtains information about a Bluetooth radio.

## -parameters

### -param hRadio

A handle to a local Bluetooth radio, obtained by calling the <a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindfirstradio">BluetoothFindFirstRadio</a> or similar functions, or the <b>SetupDiEnumerateDeviceInterfances</b> function.

### -param pRadioInfo

A pointer to a <a href="/windows/desktop/api/bluetoothapis/ns-bluetoothapis-bluetooth_radio_info">BLUETOOTH_RADIO_INFO</a> structure into which information about the radio will be placed. The <b>dwSize</b> member of the <b>BLUETOOTH_RADIO_INFO</b> structure must match the size of the structure.

## -returns

The following table  lists common return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The radio information was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>hRadio</i> or <i>pRadioInfo</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_REVISION_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The <b>dwSize</b> member of the <a href="/windows/desktop/api/bluetoothapis/ns-bluetoothapis-bluetooth_radio_info">BLUETOOTH_RADIO_INFO</a> structure pointed to by <i>pRadioInfo</i> is not valid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_find_radio_params">BLUETOOTH_FIND_RADIO_PARAMS</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindfirstradio">BluetoothFindFirstRadio</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindnextradio">BluetoothFindNextRadio</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindradioclose">BluetoothFindRadioClose</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>