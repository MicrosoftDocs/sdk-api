---
UID: NF:bluetoothapis.BluetoothSdpEnumAttributes
title: BluetoothSdpEnumAttributes function
author: windows-sdk-content
description: The BluetoothSdpEnumAttributes function enumerates through the SDP record stream, and calls the callback function for each attribute in the record.
old-location: bluetooth\bluetoothsdpenumattributes.htm
tech.root: Bluetooth
ms.assetid: 3113db03-a32f-47ad-a442-3769f41ee8e7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BluetoothSdpEnumAttributes, BluetoothSdpEnumAttributes function [Bluetooth], bluetooth.bluetoothsdpenumattributes, bluetoothapis/BluetoothSdpEnumAttributes
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - BluetoothSdpEnumAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- BluetoothSdpEnumAttributes
: 
---

# BluetoothSdpEnumAttributes function


## -description


The <b>BluetoothSdpEnumAttributes</b> function enumerates through the SDP record stream, and  calls the callback function
for each attribute in the record.


## -parameters




### -param pSDPStream

Pointer to a valid record stream that is formatted as a single SDP record.


### -param cbStreamSize

Size of the stream pointed to by <i>pSDPStream</i>, in bytes.


### -param pfnCallback

Pointer to the callback routine. See <a href="https://msdn.microsoft.com/4d728467-1866-428f-9e66-a45b597a226a">PFN_BLUETOOTH_ENUM_ATTRIBUTES_CALLBACK</a> for more information about the callback.


### -param pvParam

Optional parameter to be passed to the callback routine.


## -returns



Returns <b>TRUE</b> if an enumeration occurred. Returns <b>FALSE</b> upon failure. Call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function for more information. The following table describes common error codes associated with the <b>BluetoothSdpEnumAttributes</b> function:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pSDPStream</i> or <i>pfnCallback</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The SDP stream is corrupt.

</td>
</tr>
</table>
 




## -remarks



If the callback function returns
<b>FALSE</b>, the enumeration initiated by the <b>BluetoothSdpEnumAttributes</b> function is stopped.

The record stream in <i>pSDPStream</i>must be an SDP stream formatted as an SDP record, a SEQUENCE
containing attribute ID (UINT16) plus attribute value (any SDP element type) pairs.




## -see-also




<a href="https://msdn.microsoft.com/7dbf44f6-8a80-419e-9db7-60ada9ca9647">BluetoothSdpGetContainerElementData</a>



<a href="https://msdn.microsoft.com/65de8f2f-1781-44fa-87a9-21aa461eb8ee">BluetoothSdpGetElementData</a>



<a href="https://msdn.microsoft.com/26a68fe3-6ffb-44ff-b9db-757d35022a41">BluetoothSdpGetString</a>



<a href="https://msdn.microsoft.com/4d728467-1866-428f-9e66-a45b597a226a">PFN_BLUETOOTH_ENUM_ATTRIBUTES_CALLBACK</a>



<a href="https://msdn.microsoft.com/9c9d6103-cc49-41d2-bbb3-6b6888fb93e7">SDP_ELEMENT_DATA</a>



<a href="https://msdn.microsoft.com/16ff7951-08a7-49c5-93a5-0782cca50dab">SDP_STRING_TYPE_DATA</a>
 

 

