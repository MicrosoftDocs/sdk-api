---
UID: NF:bluetoothapis.BluetoothSdpGetAttributeValue
title: BluetoothSdpGetAttributeValue function
author: windows-driver-content
description: The BluetoothSdpGetAttributeValue function retrieves the attribute value for an attribute identifier.
old-location: bluetooth\bluetoothsdpgetattributevalue.htm
old-project: Bluetooth
ms.assetid: 79368265-3d01-4bfd-ba71-930696e0bc08
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: BluetoothSdpGetAttributeValue, BluetoothSdpGetAttributeValue function [Bluetooth], bluetooth.bluetoothsdpgetattributevalue, bluetoothapis/BluetoothSdpGetAttributeValue
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
req.typenames: BLUETOOTH_IO_CAPABILITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Bthprops.dll
-	BluetoothAPIs.dll
-	Ext-MS-Win-Bluetooth-APIs-l1-1-0.dll
api_name:
-	BluetoothSdpGetAttributeValue
product: Windows
targetos: Windows
req.lib: Bthprops.lib
req.dll: Bthprops.dll
req.irql: 
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

Pointer to an <a href="https://msdn.microsoft.com/9c9d6103-cc49-41d2-bbb3-6b6888fb93e7">SDP_ELEMENT_DATA</a> structure into which the attribute's identifier value is placed.


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



The record stream in <i>pRecordStream</i>
must be an SDP stream formatted as an SDP record, a SEQUENCE
containing attribute ID (UINT16) plus attribute value (any SDP element type) pairs.

The attribute identifier provided in the <i>usAttributeId</i> parameter can be one of the many SDP_ATTRIB_Xxx universal attribute identifiers provided in the bthdef.h file, or a custom attribute value defined by a Bluetooth profile. All values greater than or equal to 0x200 are profile-specific attribute identifiers, and are specific to the profile. See the bthdef.h header file for a list of universal SDP attribute identifiers.




## -see-also




<a href="https://msdn.microsoft.com/3113db03-a32f-47ad-a442-3769f41ee8e7">BluetoothSdpEnumAttributes</a>



<a href="https://msdn.microsoft.com/7dbf44f6-8a80-419e-9db7-60ada9ca9647">BluetoothSdpGetContainerElementData</a>



<a href="https://msdn.microsoft.com/65de8f2f-1781-44fa-87a9-21aa461eb8ee">BluetoothSdpGetElementData</a>



<a href="https://msdn.microsoft.com/26a68fe3-6ffb-44ff-b9db-757d35022a41">BluetoothSdpGetString</a>



<a href="https://msdn.microsoft.com/9c9d6103-cc49-41d2-bbb3-6b6888fb93e7">SDP_ELEMENT_DATA</a>



<a href="https://msdn.microsoft.com/16ff7951-08a7-49c5-93a5-0782cca50dab">SDP_STRING_TYPE_DATA</a>
 

 

