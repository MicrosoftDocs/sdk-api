---
UID: NS:ws2bth._BTH_SET_SERVICE
title: BTH_SET_SERVICE (ws2bth.h)
description: Provides service information for the specified Bluetooth service.
helpviewer_keywords: ["*PBTHNS_SETBLOB","*PBTH_SET_SERVICE","BTHNS_SETBLOB","BTH_SET_SERVICE","BTH_SET_SERVICE structure [Bluetooth]","PBTH_SET_SERVICE","PBTH_SET_SERVICE structure pointer [Bluetooth]","_bth_bth_set_service","bluetooth.bth_set_service","ws2bth/BTH_SET_SERVICE","ws2bth/PBTH_SET_SERVICE"]
old-location: bluetooth\bth_set_service.htm
tech.root: bluetooth
ms.assetid: 66b5474d-ea21-4ae4-9297-9740f1bc9ecb
ms.date: 12/05/2018
ms.keywords: '*PBTHNS_SETBLOB, *PBTH_SET_SERVICE, BTHNS_SETBLOB, BTH_SET_SERVICE, BTH_SET_SERVICE structure [Bluetooth], PBTH_SET_SERVICE, PBTH_SET_SERVICE structure pointer [Bluetooth], _bth_bth_set_service, bluetooth.bth_set_service, ws2bth/BTH_SET_SERVICE, ws2bth/PBTH_SET_SERVICE'
req.header: ws2bth.h
req.include-header: 
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
req.typenames: BTH_SET_SERVICE, *PBTH_SET_SERVICE, BTHNS_SETBLOB, *PBTHNS_SETBLOB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BTH_SET_SERVICE
 - ws2bth/_BTH_SET_SERVICE
 - PBTH_SET_SERVICE
 - ws2bth/PBTH_SET_SERVICE
 - BTH_SET_SERVICE
 - ws2bth/BTH_SET_SERVICE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2bth.h
api_name:
 - BTH_SET_SERVICE
---

# BTH_SET_SERVICE structure


## -description

The 
<b>BTH_SET_SERVICE</b> structure provides service information for the specified Bluetooth service.

## -struct-fields

### -field pSdpVersion

Version of the SDP. Clients set this member to 
BTH_SDP_VERSION.

### -field pRecordHandle

Handle to the SDP record. Corresponds to SDP ServiceRecordHandle. Returned by the add record operations, and subsequently used to delete the record.

### -field fCodService

Class of device (COD) information. A 32-bit field of COD_SERVICE_* class of device bits associated with this SDP record. The system  combines these bits with COD bits from other service records and system characteristics.  The resulting class of device for the local radio is advertised when the radio is found during device inquiry. When the last SDP record associated with a particular service bit is deleted, that service bit is no longer reported in responses to future device inquiries.

The format and possible values for the COD field are defined in the <i>Bluetooth Assigned Numbers 1.1</i> portion of the Bluetooth specification, Section 1.2. (This resource may not be available in some languages and countries.) Corresponding macros and definitions for COD_SERVICE_* bits used by Windows are defined in Bthdef.h. For more information about class of device (COD), see <a href="/windows/desktop/api/bthdef/ns-bthdef-bth_device_info">BTH_DEVICE_INFO</a>.

### -field Reserved

Reserved. Must be set to zero.

### -field ulRecordLength

Size, in bytes, of <b>pRecord</b>.

### -field pRecord

SDP record, as defined by the Bluetooth specification.

## -remarks

When using the 
<b>BTH_SET_SERVICE</b> structure to query services and devices using the 
<a href="/windows/desktop/Bluetooth/bluetooth-and-wsasetservice">WSASetService</a> function and 
<a href="/windows/desktop/Bluetooth/bluetooth-and-wsaqueryset-for-service-inquiry">WSAQUERYSET</a> and 
<a href="/windows/desktop/Bluetooth/bluetooth-and-blob">BLOB</a> structures. The following values for 
<b>BTH_SET_SERVICE</b> members must be used.

For more information about class of device (COD), see the Bluetooth specification at 
<a href="https://www.bluetooth.com/">www.bluetooth.com</a>.<table>
<tr>
<th>Member</th>
<th>Required value</th>
</tr>
<tr>
<td><b>pSdpVersion</b></td>
<td>Pointer to ULONG version, which is changed whenever the binary format of SDP records change, affecting the format of the <b>pRecord</b> member. Set to <b>BTH_SDP_VERSION</b> for the client, and returned by the system.</td>
</tr>
<tr>
<td><b>pRecordHandle</b></td>
<td>Handle to the SDP record; corresponds to SDP ServiceRecordHandle. Returned by the add record operations, and subsequently used to delete the record.</td>
</tr>
<tr>
<td><b>fOptions</b></td>
<td>Attributes defined by <b>BTHNS_SET_FLAGS</b>.</td>
</tr>
<tr>
<td><b>ulRecordLength</b></td>
<td>Length, in bytes, of the binary SDP record pointed to by <b>pRecord</b>.</td>
</tr>
<tr>
<td><b>pRecord</b></td>
<td>Pointer to a valid SDP record, in the format defined by the Bluetooth specification.</td>
</tr>
</table>
 



The <b>pRecordHandle</b> member must point to data that is null for new service registration. For service deletion, <b>pRecordHandle</b> must point to a valid handle. The <b>pRecord</b> member must contain the entire SD service record, as described in the Bluetooth specification. For RFCOMM protocol entries, the port number is the same as the port returned by the 
<a href="/windows/desktop/Bluetooth/bluetooth-and-getsockname">getsockname</a> function call.

Bluetooth implements a one-to-one correlation between SDP records and server sockets. As such, there is no need for the <b>SERVICE_MULTIPLE</b> flag.

## -see-also

<a href="/windows/desktop/Bluetooth/bluetooth-and-getsockname">Bluetooth
		  and getsockname</a>



<a href="/windows/desktop/Bluetooth/bluetooth-and-blob">Bluetooth and
		  BLOB</a>



<a href="/windows/desktop/Bluetooth/bluetooth-and-wsasetservice">Bluetooth and WSASetService</a>



<a href="/windows/desktop/Bluetooth/bluetooth-and-wsaqueryset-for-service-inquiry">WSAQUERYSET</a>