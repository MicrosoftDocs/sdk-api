---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# BluetoothGetRadioInfo function


## -description


The <b>BluetoothGetRadioInfo</b> function obtains information about a Bluetooth radio.


## -parameters




### -param hRadio

A handle to a local Bluetooth radio, obtained by calling the <a href="https://msdn.microsoft.com/f31bb18b-c129-417f-ab87-cf114a2e094f">BluetoothFindFirstRadio</a> or similar functions, or the <b>SetupDiEnumerateDeviceInterfances</b> function.


### -param pRadioInfo

A pointer to a <a href="https://msdn.microsoft.com/14440e02-ff2e-4fae-aac9-1b2fd936510e">BLUETOOTH_RADIO_INFO</a> structure into which information about the radio will be placed. The <b>dwSize</b> member of the <b>BLUETOOTH_RADIO_INFO</b> structure must match the size of the structure.


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
The <b>dwSize</b> member of the <a href="https://msdn.microsoft.com/14440e02-ff2e-4fae-aac9-1b2fd936510e">BLUETOOTH_RADIO_INFO</a> structure pointed to by <i>pRadioInfo</i> is not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b997203d-e7e4-43aa-b751-e419483020ac">BLUETOOTH_FIND_RADIO_PARAMS</a>



<a href="https://msdn.microsoft.com/f31bb18b-c129-417f-ab87-cf114a2e094f">BluetoothFindFirstRadio</a>



<a href="https://msdn.microsoft.com/7dd6b823-f9c6-4375-80b6-d59c4570c8fb">BluetoothFindNextRadio</a>



<a href="https://msdn.microsoft.com/859771b1-d06c-414b-81cb-bb3913fd0380">BluetoothFindRadioClose</a>



<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>
 

 

