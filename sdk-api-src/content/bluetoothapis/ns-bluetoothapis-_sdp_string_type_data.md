---
UID: NS:bluetoothapis._SDP_STRING_TYPE_DATA
title: "_SDP_STRING_TYPE_DATA"
author: windows-sdk-content
description: The SDP_STRING_TYPE_DATA structure stores information about SDP string types.
old-location: bluetooth\sdp_string_type_data.htm
tech.root: bluetooth
ms.assetid: 16ff7951-08a7-49c5-93a5-0782cca50dab
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PSDP_STRING_TYPE_DATA, *PSDP_STRING_TYPE_DATA structure [Bluetooth], SDP_STRING_TYPE_DATA, SDP_STRING_TYPE_DATA structure [Bluetooth], _SDP_STRING_TYPE_DATA, bluetooth.sdp_string_type_data, bluetoothapis/*PSDP_STRING_TYPE_DATA, bluetoothapis/SDP_STRING_TYPE_DATA"
ms.prod: windows
ms.technology: windows-sdk
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




<a href="https://msdn.microsoft.com/3113db03-a32f-47ad-a442-3769f41ee8e7">BluetoothSdpEnumAttributes</a>



<a href="https://msdn.microsoft.com/79368265-3d01-4bfd-ba71-930696e0bc08">BluetoothSdpGetAttributeValue</a>



<a href="https://msdn.microsoft.com/7dbf44f6-8a80-419e-9db7-60ada9ca9647">BluetoothSdpGetContainerElementData</a>



<a href="https://msdn.microsoft.com/65de8f2f-1781-44fa-87a9-21aa461eb8ee">BluetoothSdpGetElementData</a>



<a href="https://msdn.microsoft.com/26a68fe3-6ffb-44ff-b9db-757d35022a41">BluetoothSdpGetString</a>



<a href="https://msdn.microsoft.com/4d728467-1866-428f-9e66-a45b597a226a">PFN_BLUETOOTH_ENUM_ATTRIBUTES_CALLBACK</a>



<a href="https://msdn.microsoft.com/9c9d6103-cc49-41d2-bbb3-6b6888fb93e7">SDP_ELEMENT_DATA</a>
 

 

