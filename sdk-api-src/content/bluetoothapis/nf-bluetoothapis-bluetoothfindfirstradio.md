---
UID: NF:bluetoothapis.BluetoothFindFirstRadio
title: BluetoothFindFirstRadio function (bluetoothapis.h)
description: The BluetoothFindFirstRadio function begins the enumeration of local Bluetooth radios.
helpviewer_keywords: ["BluetoothFindFirstRadio","BluetoothFindFirstRadio function [Bluetooth]","bluetooth.bluetoothfindfirstradio","bluetoothapis/BluetoothFindFirstRadio"]
old-location: bluetooth\bluetoothfindfirstradio.htm
tech.root: bluetooth
ms.assetid: f31bb18b-c129-417f-ab87-cf114a2e094f
ms.date: 12/05/2018
ms.keywords: BluetoothFindFirstRadio, BluetoothFindFirstRadio function [Bluetooth], bluetooth.bluetoothfindfirstradio, bluetoothapis/BluetoothFindFirstRadio
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
 - BluetoothFindFirstRadio
 - bluetoothapis/BluetoothFindFirstRadio
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
 - BluetoothFindFirstRadio
---

# BluetoothFindFirstRadio function


## -description

The <b>BluetoothFindFirstRadio</b> function begins the enumeration of local Bluetooth radios.

## -parameters

### -param pbtfrp

Pointer to a <a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_find_radio_params">BLUETOOTH_FIND_RADIO_PARAMS</a> structure. The <b>dwSize</b> member of the <b>BLUETOOTH_FIND_RADIO_PARAMS</b> structure pointed to by <i>pbtfrp</i> must match the size of the structure.

### -param phRadio [out]

Pointer to where the first enumerated radio handle will be returned. When no longer needed, this handle must be closed via <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.

## -returns

In addition to the handle indicated by <i>phRadio</i>, calling this function will also create a HBLUETOOTH_RADIO_FIND handle for use with the <a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindnextradio">BluetoothFindNextRadio</a> function. When this handle is no longer needed, it must be closed via the <a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindradioclose">BluetoothFindRadioClose</a>.

Returns <b>NULL</b> upon failure. Call the  <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function for more information on the error. The following table  describe common errors:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
No Bluetooth radios found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pbtfrp</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_REVISION_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The structure pointed to by <i>pbtfrp</i> is not the correct size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>

## -see-also

<a href="/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_find_radio_params">BLUETOOTH_FIND_RADIO_PARAMS</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindnextradio">BluetoothFindNextRadio</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindradioclose">BluetoothFindRadioClose</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothgetradioinfo">BluetoothGetRadioInfo</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>