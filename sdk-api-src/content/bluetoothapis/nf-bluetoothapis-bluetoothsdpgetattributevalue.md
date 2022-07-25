---
UID: NF:bluetoothapis.BluetoothSdpGetAttributeValue
title: BluetoothSdpGetAttributeValue function (bluetoothapis.h)
description: The BluetoothSdpGetAttributeValue function retrieves the attribute value for an attribute identifier.
helpviewer_keywords: ["BluetoothSdpGetAttributeValue","BluetoothSdpGetAttributeValue function [Bluetooth]","bluetooth.bluetoothsdpgetattributevalue","bluetoothapis/BluetoothSdpGetAttributeValue"]
old-location: bluetooth\bluetoothsdpgetattributevalue.htm
tech.root: bluetooth
ms.assetid: 79368265-3d01-4bfd-ba71-930696e0bc08
ms.date: 12/05/2018
ms.keywords: BluetoothSdpGetAttributeValue, BluetoothSdpGetAttributeValue function [Bluetooth], bluetooth.bluetoothsdpgetattributevalue, bluetoothapis/BluetoothSdpGetAttributeValue
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
 - BluetoothSdpGetAttributeValue
 - bluetoothapis/BluetoothSdpGetAttributeValue
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
 - BluetoothSdpGetAttributeValue
---

# BluetoothSdpGetAttributeValue function


## -description

The <b>BluetoothSdpGetAttributeValue</b> function retrieves the attribute value for an attribute identifier.

## -parameters

### -param pRecordStream [in]

Pointer to a valid record stream that is formatted as a single SDP record.

### -param cbRecordLength [in]

Length of <i>pRecordStream</i>, in bytes.

### -param usAttributeId [in]

Attribute identifier to search for. See Remarks.

### -param pAttributeData [out]

Pointer to an <a href="/windows/desktop/api/bluetoothapis/ns-bluetoothapis-sdp_element_data">SDP_ELEMENT_DATA</a> structure into which the attribute's identifier value is placed.

## -returns

Returns ERROR_SUCCESS upon successful completion; the <i>pAddributeData</i> parameter contains the attribute value. Any other return value indicates error. The following table describes common error codes associated with the <b>BluetoothSdpGetAttributeValue</b> function:

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
Either one of the required pointers was <b>NULL</b>, the <i>pRecordStream</i> parameter was not a valid SDP stream, or the <i>pRecordStream</i> parameter was not a properly formatted SDP record.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The identifier provided in <i>usAttributeId</i> was not found in the record.

</td>
</tr>
</table>

## -remarks

The record stream in <i>pRecordStream</i> must be an SDP stream formatted as an SDP record, a SEQUENCE
containing attribute ID (UINT16) plus attribute value (any SDP element type) pairs.

The attribute identifier provided in the <i>usAttributeId</i> parameter can be one of the many SDP_ATTRIB_Xxx universal attribute identifiers provided in the bthdef.h file, or a custom attribute value defined by a Bluetooth profile. All values greater than or equal to 0x200 are profile-specific attribute identifiers, and are specific to the profile. See the bthdef.h header file for a list of universal SDP attribute identifiers.

## -see-also

<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpenumattributes">BluetoothSdpEnumAttributes</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpgetcontainerelementdata">BluetoothSdpGetContainerElementData</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpgetelementdata">BluetoothSdpGetElementData</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpgetstring">BluetoothSdpGetString</a>



<a href="/windows/desktop/api/bluetoothapis/ns-bluetoothapis-sdp_element_data">SDP_ELEMENT_DATA</a>



<a href="/windows/desktop/api/bluetoothapis/ns-bluetoothapis-sdp_string_type_data">SDP_STRING_TYPE_DATA</a>