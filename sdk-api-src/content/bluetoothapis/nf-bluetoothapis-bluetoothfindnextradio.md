---
UID: NF:bluetoothapis.BluetoothFindNextRadio
title: BluetoothFindNextRadio function (bluetoothapis.h)
description: The BluetoothFindNextRadio function finds the next Bluetooth radio.
helpviewer_keywords: ["BluetoothFindNextRadio","BluetoothFindNextRadio function [Bluetooth]","bluetooth.bluetoothfindnextradio","bluetoothapis/BluetoothFindNextRadio"]
old-location: bluetooth\bluetoothfindnextradio.htm
tech.root: bluetooth
ms.assetid: 7dd6b823-f9c6-4375-80b6-d59c4570c8fb
ms.date: 12/05/2018
ms.keywords: BluetoothFindNextRadio, BluetoothFindNextRadio function [Bluetooth], bluetooth.bluetoothfindnextradio, bluetoothapis/BluetoothFindNextRadio
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
 - BluetoothFindNextRadio
 - bluetoothapis/BluetoothFindNextRadio
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
 - BluetoothFindNextRadio
---

# BluetoothFindNextRadio function


## -description

The <b>BluetoothFindNextRadio</b> function finds the next Bluetooth radio.

## -parameters

### -param hFind [in]

Handle returned by a previous call to the <a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindfirstradio">BluetoothFindFirstRadio</a> function. Use <a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindradioclose">BluetoothFindRadioClose</a> to close this handle when it is no longer needed.

### -param phRadio [out]

Pointer to where the next enumerated radio handle will be returned.  When no longer needed, this handle must be released via <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.

## -returns

Returns <b>TRUE</b> when the next available radio is found.

Returns <b>FALSE</b> when no new radios are found.  Call the  <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function for more information on the error. The following table  describe common errors:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
No more radios were found.

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



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindfirstradio">BluetoothFindFirstRadio</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothfindradioclose">BluetoothFindRadioClose</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothgetradioinfo">BluetoothGetRadioInfo</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>