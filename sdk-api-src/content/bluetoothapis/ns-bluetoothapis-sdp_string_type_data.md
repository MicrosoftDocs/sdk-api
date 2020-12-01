---
UID: NS:bluetoothapis._SDP_STRING_TYPE_DATA
title: SDP_STRING_TYPE_DATA (bluetoothapis.h)
description: The SDP_STRING_TYPE_DATA structure stores information about SDP string types.
helpviewer_keywords: ["*PSDP_STRING_TYPE_DATA","*PSDP_STRING_TYPE_DATA structure [Bluetooth]","SDP_STRING_TYPE_DATA","SDP_STRING_TYPE_DATA structure [Bluetooth]","bluetooth.sdp_string_type_data","bluetoothapis/*PSDP_STRING_TYPE_DATA","bluetoothapis/SDP_STRING_TYPE_DATA"]
old-location: bluetooth\sdp_string_type_data.htm
tech.root: bluetooth
ms.assetid: 16ff7951-08a7-49c5-93a5-0782cca50dab
ms.date: 12/05/2018
ms.keywords: '*PSDP_STRING_TYPE_DATA, *PSDP_STRING_TYPE_DATA structure [Bluetooth], SDP_STRING_TYPE_DATA, SDP_STRING_TYPE_DATA structure [Bluetooth], bluetooth.sdp_string_type_data, bluetoothapis/*PSDP_STRING_TYPE_DATA, bluetoothapis/SDP_STRING_TYPE_DATA'
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
req.typenames: SDP_STRING_TYPE_DATA, *PSDP_STRING_TYPE_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SDP_STRING_TYPE_DATA
 - bluetoothapis/_SDP_STRING_TYPE_DATA
 - PSDP_STRING_TYPE_DATA
 - bluetoothapis/PSDP_STRING_TYPE_DATA
 - SDP_STRING_TYPE_DATA
 - bluetoothapis/SDP_STRING_TYPE_DATA
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
 - SDP_STRING_TYPE_DATA
---

## -description

The <b>SDP_STRING_TYPE_DATA</b> structure stores information about SDP string types.

## -struct-fields

### -field encoding

Specifies how the string is encoded according to ISO 639:1988 (E/F): Code for the representation of the names of languages.

### -field mibeNum

MIBE number from the IANA database.

### -field attributeId

Identifier of the base attribute in which the string is to be found in the record.

## -see-also

<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpenumattributes">BluetoothSdpEnumAttributes</a>

<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpgetattributevalue">BluetoothSdpGetAttributeValue</a>

<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpgetcontainerelementdata">BluetoothSdpGetContainerElementData</a>

<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpgetelementdata">BluetoothSdpGetElementData</a>

<a href="/windows/desktop/api/bluetoothapis/nf-bluetoothapis-bluetoothsdpgetstring">BluetoothSdpGetString</a>

<a href="/windows/desktop/api/bluetoothapis/nc-bluetoothapis-pfn_bluetooth_enum_attributes_callback">PFN_BLUETOOTH_ENUM_ATTRIBUTES_CALLBACK</a>

<a href="/windows/desktop/api/bluetoothapis/ns-bluetoothapis-sdp_element_data">SDP_ELEMENT_DATA</a>