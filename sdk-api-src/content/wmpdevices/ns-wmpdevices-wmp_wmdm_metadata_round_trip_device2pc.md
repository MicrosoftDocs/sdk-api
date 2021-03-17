---
UID: NS:wmpdevices._WMP_WMDM_METADATA_ROUND_TRIP_DEVICE2PC
title: WMP_WMDM_METADATA_ROUND_TRIP_DEVICE2PC (wmpdevices.h)
description: The WMP_WMDM_METADATA_ROUND_TRIP_DEVICE2PC structure is used by Windows Media Player to receive accelerated metadata synchronization information from portable devices that do not support MTP.
helpviewer_keywords: ["WMP_MDRT_FLAGS_UNREPORTED_ADDED_ITEMS","WMP_MDRT_FLAGS_UNREPORTED_DELETED_ITEMS","WMP_WMDM_DEVICE2PC","WMP_WMDM_METADATA_ROUND_TRIP_DEVICE2PC","WMP_WMDM_METADATA_ROUND_TRIP_DEVICE2PC structure [Windows Media Player]","wmp.wmp_wmdm_metadata_round_trip_device2pc","wmpdevices/WMP_WMDM_METADATA_ROUND_TRIP_DEVICE2PC"]
old-location: wmp\wmp_wmdm_metadata_round_trip_device2pc.htm
tech.root: WMP
ms.assetid: aadcbeda-97c4-4902-a1c4-31e71d27ae40
ms.date: 12/05/2018
ms.keywords: WMP_MDRT_FLAGS_UNREPORTED_ADDED_ITEMS, WMP_MDRT_FLAGS_UNREPORTED_DELETED_ITEMS, WMP_WMDM_DEVICE2PC, WMP_WMDM_METADATA_ROUND_TRIP_DEVICE2PC, WMP_WMDM_METADATA_ROUND_TRIP_DEVICE2PC structure [Windows Media Player], wmp.wmp_wmdm_metadata_round_trip_device2pc, wmpdevices/WMP_WMDM_METADATA_ROUND_TRIP_DEVICE2PC
req.header: wmpdevices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 10 or later.
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WMP_WMDM_METADATA_ROUND_TRIP_DEVICE2PC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WMP_WMDM_METADATA_ROUND_TRIP_DEVICE2PC
 - wmpdevices/_WMP_WMDM_METADATA_ROUND_TRIP_DEVICE2PC
 - WMP_WMDM_METADATA_ROUND_TRIP_DEVICE2PC
 - wmpdevices/WMP_WMDM_METADATA_ROUND_TRIP_DEVICE2PC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wmpdevices.h
api_name:
 - WMP_WMDM_METADATA_ROUND_TRIP_DEVICE2PC
---

# WMP_WMDM_METADATA_ROUND_TRIP_DEVICE2PC structure


## -description

The <b>WMP_WMDM_METADATA_ROUND_TRIP_DEVICE2PC</b> structure is used by Windows Media Player to receive accelerated metadata synchronization information from portable devices that do not support MTP.

## -struct-fields

### -field dwCurrentTransactionID

The current transaction ID for the device. Windows Media Player stores this value and uses it for future requests.

### -field dwReturnedObjectCount

The number of object path names returned in the <b>wsObjectPathnameList</b> member.

### -field dwUnretrievedObjectCount

The number of objects that were changed or deleted, but that are not part of this response. A value greater than zero signals Windows Media Player to make a further request.

### -field dwDeletedObjectStartingOffset

The index of the first character of the first deleted object path name. If the path name list contains only deleted objects, specify zero. If the path name list contains no deleted objects, specify the index of the last null character in the path name list. Note that this value is the number of Unicode characters to skip in <b>wsObjectPathnameList</b>, not the number of bytes.

### -field dwFlags

The status information. Status is indicated in a bitwise fashion by using the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WMP_MDRT_FLAGS_UNREPORTED_DELETED_ITEMS"></a><a id="wmp_mdrt_flags_unreported_deleted_items"></a><dl>
<dt><b>WMP_MDRT_FLAGS_UNREPORTED_DELETED_ITEMS</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Items were deleted before the first object path name being reported. This often indicates that the device was reformatted.

</td>
</tr>
<tr>
<td width="40%"><a id="WMP_MDRT_FLAGS_UNREPORTED_ADDED_ITEMS"></a><a id="wmp_mdrt_flags_unreported_added_items"></a><dl>
<dt><b>WMP_MDRT_FLAGS_UNREPORTED_ADDED_ITEMS</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Some additional items were added that were not returned in the list of PUOIDs.

</td>
</tr>
</table>
 

Bits 2 through 31 are reserved for future use. These bits should be set to zero.

### -field wsObjectPathnameList

Contains a contiguous list of null terminated Unicode path name strings, terminated with an extra null character. The list must be created in the following manner:

First, path name strings for all objects that have been added to the device or have had a change for the PlayCount, UserRating, or BuyNow attributes.

Second, path name strings for all objects that have been deleted. The index of the first character of this part of the list is contained in the <b>dwDeletedObjectStartingOffset</b> member.

## -remarks

The Windows Media Device Manager service provider should return as many object path names as will fit in the buffer size specified by the <i>pnOutBufferSize</i> parameter of the <b>DeviceIoControl</b> method. If the buffer is not large enough to contain the path name strings for all the changes, the device must set the <b>dwUnretrievedObjectCount</b> member to the appropriate (nonzero) value.

## -see-also

<a href="/windows/desktop/WMP/windows-media-device-manager-device-extensions-for-metadata-transfer">Windows Media Device Manager Device Extensions for Metadata Transfer</a>