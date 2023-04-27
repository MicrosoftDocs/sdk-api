---
UID: NF:bluetoothapis.BluetoothSdpGetString
title: BluetoothSdpGetString function (bluetoothapis.h)
description: Converts a raw string embedded in the SDP record into a Unicode string.
helpviewer_keywords: ["BluetoothSdpGetString","BluetoothSdpGetString function [Bluetooth]","bluetooth.bluetoothsdpgetstring","bluetoothapis/BluetoothSdpGetString"]
old-location: bluetooth\bluetoothsdpgetstring.htm
tech.root: bluetooth
ms.assetid: 26a68fe3-6ffb-44ff-b9db-757d35022a41
ms.date: 12/05/2018
ms.keywords: BluetoothSdpGetString, BluetoothSdpGetString function [Bluetooth], bluetooth.bluetoothsdpgetstring, bluetoothapis/BluetoothSdpGetString
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
 - BluetoothSdpGetString
 - bluetoothapis/BluetoothSdpGetString
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
 - BluetoothSdpGetString
---

# BluetoothSdpGetString function


## -description

The <b>BluetoothSdpGetString</b> function converts a raw string embedded in the SDP record into a Unicode string.

## -parameters

### -param pRecordStream [in]

A pointer to a valid record stream formatted as a single SDP record.

### -param cbRecordLength [in]

The length, in bytes, of <i>pRecordStream</i>.

### -param pStringData [in]

When set to <b>NULL</b>, the calling thread locale is used to search          for a matching string in the SDP record.  If not <b>NULL</b>, the <b>mibeNum</b> and <b>attributeId</b> members of the 
<a href="/windows/desktop/api/bluetoothapis/ns-bluetoothapis-sdp_string_type_data">SDP_STRING_TYPE_DATA</a> structure are used to find the string to convert.

### -param usStringOffset [in]

SDP string type offset to convert.  The <i>usStringOffset</i> is added to the base attribute identifier  of the string.   SDP specification-defined offsets are: STRING_NAME_OFFSET, STRING_DESCRIPTION_OFFSET, and STRING_PROVIDER_NAME_OFFSET. These offsets can be found in the bthdef.h header file.

### -param pszString [out]

If not <b>NULL</b>, contains the converted string on output. When set to <b>NULL</b>, the <i>pcchStringLength</i> parameter is filled with the required number of characters, not bytes, to retrieve the converted string.

### -param pcchStringLength [in, out]

On input, contains the length of
<i>pszString</i> if <i>pszString</i> is not <b>NULL</b>, in characters.

Upon output, contains the
number of required characters including <b>NULL</b> if an error is returned,
or the number of characters written to <i>pszString</i>, including <b>NULL</b>.

## -returns

Returns ERROR_SUCCESS upon successful completion; the <i>pszString</i> parameter contains the converted string. Returns error codes upon failure. Common errors are listed in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The <i>pszString</i> parameter was <b>NULL</b> or too small to contain the converted string; the <i>pcchStringLength</i> parameter contains, in characters, the required length.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The conversion cannot be performed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SYSTEM_RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
The system cannot allocate memory internally to perform the conversion.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the required pointers was <b>NULL</b>, the <i>pRecordStream</i> parameter was not a valid
SDP stream, the <i>pRecordStream</i> was not a properly formatted record, or
the requested attribute plus offset was not a string.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpenumattributes">BluetoothSdpEnumAttributes</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpgetattributevalue">BluetoothSdpGetAttributeValue</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpgetcontainerelementdata">BluetoothSdpGetContainerElementData</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpgetelementdata">BluetoothSdpGetElementData</a>



<a href="/windows/desktop/api/bluetoothapis/ns-bluetoothapis-sdp_element_data">SDP_ELEMENT_DATA</a>



<a href="/windows/desktop/api/bluetoothapis/ns-bluetoothapis-sdp_string_type_data">SDP_STRING_TYPE_DATA</a>