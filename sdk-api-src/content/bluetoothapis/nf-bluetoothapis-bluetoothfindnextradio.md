---
UID: NF:bluetoothapis.BluetoothFindNextRadio
title: BluetoothFindNextRadio function (bluetoothapis.h)
author: windows-sdk-content
description: The BluetoothFindNextRadio function finds the next Bluetooth radio.
old-location: bluetooth\bluetoothfindnextradio.htm
tech.root: bluetooth
ms.assetid: 7dd6b823-f9c6-4375-80b6-d59c4570c8fb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BluetoothFindNextRadio, BluetoothFindNextRadio function [Bluetooth], bluetooth.bluetoothfindnextradio, bluetoothapis/BluetoothFindNextRadio
ms.topic: function
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
req.dll: Bthprops.dll
req.irql: 
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
 - BluetoothFindNextRadio
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# BluetoothFindNextRadio function


## -description


The <b>BluetoothFindNextRadio</b> function finds the next Bluetooth radio.


## -parameters




### -param hFind [in]

Handle returned by a previous call to the <a href="https://msdn.microsoft.com/f31bb18b-c129-417f-ab87-cf114a2e094f">BluetoothFindFirstRadio</a> function. Use <a href="https://msdn.microsoft.com/859771b1-d06c-414b-81cb-bb3913fd0380">BluetoothFindRadioClose</a> to close this handle when it is no longer needed. 


### -param phRadio [out]

Pointer to where the next enumerated radio handle will be returned.  When no longer needed, this handle must be released via <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>.


## -returns



Returns <b>TRUE</b> when the next available radio is found.

Returns <b>FALSE</b> when no new radios are found.  Call the  <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function for more information on the error. The following table  describe common errors:

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




<a href="https://msdn.microsoft.com/en-us/library/Aa362926(v=VS.85).aspx">BLUETOOTH_FIND_RADIO_PARAMS</a>



<a href="https://msdn.microsoft.com/f31bb18b-c129-417f-ab87-cf114a2e094f">BluetoothFindFirstRadio</a>



<a href="https://msdn.microsoft.com/859771b1-d06c-414b-81cb-bb3913fd0380">BluetoothFindRadioClose</a>



<a href="https://msdn.microsoft.com/0c596f49-70f9-4a58-842c-e01dcf69bd01">BluetoothGetRadioInfo</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>
 

 

