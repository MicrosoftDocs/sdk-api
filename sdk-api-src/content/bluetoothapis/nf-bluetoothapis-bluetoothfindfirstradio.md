---
UID: NF:bluetoothapis.BluetoothFindFirstRadio
title: BluetoothFindFirstRadio function
author: windows-sdk-content
description: The BluetoothFindFirstRadio function begins the enumeration of local Bluetooth radios.
old-location: bluetooth\bluetoothfindfirstradio.htm
old-project: bluetooth
ms.assetid: f31bb18b-c129-417f-ab87-cf114a2e094f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: BluetoothFindFirstRadio, BluetoothFindFirstRadio function [Bluetooth], bluetooth.bluetoothfindfirstradio, bluetoothapis/BluetoothFindFirstRadio
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: bluetoothapis.h
req.include-header: Bthsdpdef.h, BluetoothAPIs.h
req.redist: 
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
req.typenames: BLUETOOTH_IO_CAPABILITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bthprops.dll
 - BluetoothAPIs.dll
 - Ext-MS-Win-Bluetooth-APIs-l1-1-0.dll
api_name:
 - BluetoothFindFirstRadio
product: Windows
targetos: Windows
req.lib: Bthprops.lib
req.dll: Bthprops.dll
req.irql: 
---

# BluetoothFindFirstRadio function


## -description


The <b>BluetoothFindFirstRadio</b> function begins the enumeration of local Bluetooth radios.


## -parameters




### -param pbtfrp

Pointer to a <a href="https://msdn.microsoft.com/b997203d-e7e4-43aa-b751-e419483020ac">BLUETOOTH_FIND_RADIO_PARAMS</a> structure. The <b>dwSize</b> member of the <b>BLUETOOTH_FIND_RADIO_PARAMS</b> structure pointed to by <i>pbtfrp</i> must match the size of the structure.


### -param phRadio [out]

Pointer to where the first enumerated radio handle will be returned. When no longer needed, this handle must be closed via <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>.


## -returns



In addition to the handle indicated by <i>phRadio</i>, calling this function will also create a HBLUETOOTH_RADIO_FIND handle for use with the <a href="https://msdn.microsoft.com/7dd6b823-f9c6-4375-80b6-d59c4570c8fb">BluetoothFindNextRadio</a> function. When this handle is no longer needed, it must be closed via the <a href="https://msdn.microsoft.com/859771b1-d06c-414b-81cb-bb3913fd0380">BluetoothFindRadioClose</a>.

Returns <b>NULL</b> upon failure. Call the  <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function for more information on the error. The following table  describe common errors:

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




<a href="https://msdn.microsoft.com/b997203d-e7e4-43aa-b751-e419483020ac">BLUETOOTH_FIND_RADIO_PARAMS</a>



<a href="https://msdn.microsoft.com/7dd6b823-f9c6-4375-80b6-d59c4570c8fb">BluetoothFindNextRadio</a>



<a href="https://msdn.microsoft.com/859771b1-d06c-414b-81cb-bb3913fd0380">BluetoothFindRadioClose</a>



<a href="https://msdn.microsoft.com/0c596f49-70f9-4a58-842c-e01dcf69bd01">BluetoothGetRadioInfo</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>
 

 

