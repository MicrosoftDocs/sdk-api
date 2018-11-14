---
UID: NS:bluetoothapis._SDP_STRING_TYPE_DATA
title: "_SDP_STRING_TYPE_DATA"
author: windows-sdk-content
description: The SDP_STRING_TYPE_DATA structure stores information about SDP string types.
old-location: bluetooth\sdp_string_type_data.htm
tech.root: Bluetooth
ms.assetid: 16ff7951-08a7-49c5-93a5-0782cca50dab
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PSDP_STRING_TYPE_DATA, *PSDP_STRING_TYPE_DATA structure [Bluetooth], SDP_STRING_TYPE_DATA, SDP_STRING_TYPE_DATA structure [Bluetooth], _SDP_STRING_TYPE_DATA, bluetooth.sdp_string_type_data, bluetoothapis/*PSDP_STRING_TYPE_DATA, bluetoothapis/SDP_STRING_TYPE_DATA"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - BluetoothAPIs.h
api_name:
 - SDP_STRING_TYPE_DATA
product: Windows
targetos: Windows
req.typenames: SDP_STRING_TYPE_DATA, *PSDP_STRING_TYPE_DATA
req.redist: 
---

# _SDP_STRING_TYPE_DATA structure


## -description


The <b>SDP_STRING_TYPE_DATA</b> structure stores information about SDP string types.


## -struct-fields




### -field encoding

Specifies how the string is encoded according to ISO 639:1988 (E/F): Code
    for the representation of the names of languages.


### -field mibeNum

MIBE number from the IANA database.


### -field attributeId

 




#### - attributeID

Identifier of the base attribute in which the string is to be found in the record.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa362885(v=VS.85).aspx">BluetoothSdpEnumAttributes</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362886(v=VS.85).aspx">BluetoothSdpGetAttributeValue</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362887(v=VS.85).aspx">BluetoothSdpGetContainerElementData</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362889(v=VS.85).aspx">BluetoothSdpGetElementData</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362890(v=VS.85).aspx">BluetoothSdpGetString</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa362945(v=VS.85).aspx">PFN_BLUETOOTH_ENUM_ATTRIBUTES_CALLBACK</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363054(v=VS.85).aspx">SDP_ELEMENT_DATA</a>
 

 

