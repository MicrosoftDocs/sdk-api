---
UID: NS:bluetoothapis._SDP_ELEMENT_DATA
title: SDP_ELEMENT_DATA (bluetoothapis.h)
description: The SDP_ELEMENT_DATA structure stores SDP element data.
helpviewer_keywords: ["*PSDP_ELEMENT_DATA","*PSDP_ELEMENT_DATA structure [Bluetooth]","SDP_ELEMENT_DATA","SDP_ELEMENT_DATA structure [Bluetooth]","bluetooth.sdp_element_data","bluetoothapis/*PSDP_ELEMENT_DATA","bluetoothapis/SDP_ELEMENT_DATA"]
old-location: bluetooth\sdp_element_data.htm
tech.root: bluetooth
ms.assetid: 9c9d6103-cc49-41d2-bbb3-6b6888fb93e7
ms.date: 12/05/2018
ms.keywords: '*PSDP_ELEMENT_DATA, *PSDP_ELEMENT_DATA structure [Bluetooth], SDP_ELEMENT_DATA, SDP_ELEMENT_DATA structure [Bluetooth], bluetooth.sdp_element_data, bluetoothapis/*PSDP_ELEMENT_DATA, bluetoothapis/SDP_ELEMENT_DATA'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SDP_ELEMENT_DATA, *PSDP_ELEMENT_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SDP_ELEMENT_DATA
 - bluetoothapis/_SDP_ELEMENT_DATA
 - PSDP_ELEMENT_DATA
 - bluetoothapis/PSDP_ELEMENT_DATA
 - SDP_ELEMENT_DATA
 - bluetoothapis/SDP_ELEMENT_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - BluetoothAPIs.h
api_name:
 - SDP_ELEMENT_DATA
---

# SDP_ELEMENT_DATA structure


## -description

The <b>SDP_ELEMENT_DATA</b> structure stores SDP element data.

## -struct-fields

### -field type

Enumeration of SDP element types.  Generic element types have a
    <b>specificType</b> value different from SDP_ST_NONE.  The generic SDP element types are the following:


<ul>
<li>SDP_TYPE_UINT</li>
<li>SDP_TYPE_INT</li>
<li>SDP_TYPE_UUID</li>
</ul>



The following element types do not have corresponding <b>specificType</b> values:

<ul>
<li>SDP_TYPE_STRING</li>
<li>SDP_TYPE_URL</li>
<li>SDP_TYPE_SEQUENCE</li>
<li>SDP_TYPE_ALTERNATIVE</li>
<li>SDP_TYPE_BOOLEAN</li>
<li>SDP_TYPE_NIL</li>
</ul>


There is no associated data value with the type SDP_TYPE_NIL.

### -field specificType

Specific type of SDP element, used to further specify generic element types.

### -field data

### -field data.int128

Value for type equals SDP_TYPE_INT, value for <b>specificType</b> equals SDP_ST_INT128.

### -field data.int64

Value for type equals SDP_TYPE_INT, value for <b>specificType</b> equals SDP_ST_INT64.

### -field data.int32

Value for type equals SDP_TYPE_INT, value for <b>specificType</b> equals SDP_ST_INT32.

### -field data.int16

Value for type equals SDP_TYPE_INT, value for <b>specificType</b> equals SDP_ST_INT16.

### -field data.int8

Value for type equals SDP_TYPE_INT, value for <b>specificType</b> equals SDP_ST_INT8.

### -field data.uint128

Value for type equals SDP_TYPE_UINT, value for <b>specificType</b> equals SDP_ST_UINT128.

### -field data.uint64

Value for type equals SDP_TYPE_UINT, value for <b>specificType</b> equals SDP_ST_UINT64.

### -field data.uint32

Value for type equals SDP_TYPE_UINT, value for <b>specificType</b> equals SDP_ST_UINT32.

### -field data.uint16

Value for type equals SDP_TYPE_UINT, value for <b>specificType</b> equals SDP_ST_UINT16.

### -field data.uint8

Value for type equals SDP_TYPE_UINT, value for <b>specificType</b> equals SDP_ST_UINT8.

### -field data.booleanVal

Value for type equals SDP_TYPE_BOOLEAN.

### -field data.uuid128

Value for type equals SDP_TYPE_UUID, value for <b>specificType</b> equals SDP_ST_UUID128.

### -field data.uuid32

Value for type equals SDP_TYPE_UUID, value for <b>specificType</b> equals SDP_ST_UUID32.

### -field data.uuid16

Value for type equals SDP_TYPE_UUID, value for <b>specificType</b> equals SDP_ST_UUID16.

### -field data.string

### -field data.string.value

Value for type equals SDP_TYPE_STRING, which is a raw string buffer. Cannot be encoded as ANSI. Use the <a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpgetstring">BluetoothSdpGetString</a> function to convert the value if it is described by the base language attribute identifier list.

### -field data.string.length

Raw length of the string. Cannot be null terminated.

### -field data.url

### -field data.url.value

Value for type equals SDP_TYPE_URL.

### -field data.url.length

Length of the raw URL. Cannot be null terminated.

### -field data.sequence

### -field data.sequence.value

Raw sequence that begins at the sequence element header. Value for type equals SDP_TYPE_SEQUENCE.

### -field data.sequence.length

Length of the raw sequence. Cannot be null terminated.

### -field data.alternative

### -field data.alternative.value

Raw alternative that begins at the alternative element header. Value for type equals SDP_TYPE_ALTERNATIVE.

### -field data.alternative.length

Length of the raw alternative. Cannot be null terminated.

## -see-also

<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpenumattributes">BluetoothSdpEnumAttributes</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpgetattributevalue">BluetoothSdpGetAttributeValue</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpgetcontainerelementdata">BluetoothSdpGetContainerElementData</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpgetelementdata">BluetoothSdpGetElementData</a>



<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpgetstring">BluetoothSdpGetString</a>



<a href="/windows/desktop/api/bluetoothapis/nc-bluetoothapis-pfn_bluetooth_enum_attributes_callback">PFN_BLUETOOTH_ENUM_ATTRIBUTES_CALLBACK</a>