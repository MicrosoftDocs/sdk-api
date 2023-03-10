---
UID: NF:bluetoothapis.BluetoothSdpEnumAttributes
title: BluetoothSdpEnumAttributes function (bluetoothapis.h)
description: The BluetoothSdpEnumAttributes function enumerates through the SDP record stream, and calls the callback function for each attribute in the record.
helpviewer_keywords: ["BluetoothSdpEnumAttributes","BluetoothSdpEnumAttributes function [Bluetooth]","bluetooth.bluetoothsdpenumattributes","bluetoothapis/BluetoothSdpEnumAttributes"]
old-location: bluetooth\bluetoothsdpenumattributes.htm
tech.root: bluetooth
ms.assetid: 3113db03-a32f-47ad-a442-3769f41ee8e7
ms.date: 12/05/2018
ms.keywords: BluetoothSdpEnumAttributes, BluetoothSdpEnumAttributes function [Bluetooth], bluetooth.bluetoothsdpenumattributes, bluetoothapis/BluetoothSdpEnumAttributes
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
 - BluetoothSdpEnumAttributes
 - bluetoothapis/BluetoothSdpEnumAttributes
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
 - BluetoothSdpEnumAttributes
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

Pointer to the callback routine. See <a href="/windows/desktop/api/bluetoothapis/nc-bluetoothapis-pfn_bluetooth_enum_attributes_callback">PFN_BLUETOOTH_ENUM_ATTRIBUTES_CALLBACK</a> for more information about the callback.

### -param pvParam

Optional parameter to be passed to the callback routine.

## -returns

Returns <b>TRUE</b> if an enumeration occurred. Returns <b>FALSE</b> upon failure. Call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function for more information. The following table describes common error codes associated with the <b>BluetoothSdpEnumAttributes</b> function:

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

The record stream in <i>pSDPStream</i> must be an SDP stream formatted as an SDP record, a SEQUENCE
containing attribute ID (UINT16) plus attribute value (any SDP element type) pairs.

## -see-also

<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpgetcontainerelementdata">BluetoothSdpGetContainerElementData</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpgetelementdata">BluetoothSdpGetElementData</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpgetstring">BluetoothSdpGetString</a>



<a href="/windows/desktop/api/bluetoothapis/nc-bluetoothapis-pfn_bluetooth_enum_attributes_callback">PFN_BLUETOOTH_ENUM_ATTRIBUTES_CALLBACK</a>



<a href="/windows/desktop/api/bluetoothapis/ns-bluetoothapis-sdp_element_data">SDP_ELEMENT_DATA</a>



<a href="/windows/desktop/api/bluetoothapis/ns-bluetoothapis-sdp_string_type_data">SDP_STRING_TYPE_DATA</a>