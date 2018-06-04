---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
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
---

# _BTH_SET_SERVICE structure


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

The format and possible values for the COD field are defined in the <i>Bluetooth Assigned Numbers 1.1</i> portion of the Bluetooth specification, Section 1.2. (This resource may not be available in some languages and countries.) Corresponding macros and definitions for COD_SERVICE_* bits used by Windows are defined in Bthdef.h. For more information about class of device (COD), see <a href="https://msdn.microsoft.com/b0f2c1fe-1fa0-4816-8471-73fbbced529b">BTH_DEVICE_INFO</a>.


### -field Reserved

Reserved. Must be set to zero.


### -field ulRecordLength

Size, in bytes, of <b>pRecord</b>.


### -field pRecord

SDP record, as defined by the Bluetooth specification.


## -remarks



When using the 
<b>BTH_SET_SERVICE</b> structure to query services and devices using the 
<a href="https://msdn.microsoft.com/71c5ed9c-fade-4d15-848e-eb810ad4cbb2">WSASetService</a> function and 
<a href="https://msdn.microsoft.com/c52a7e7d-92ab-4103-a6c6-57c3fafec706">WSAQUERYSET</a> and 
<a href="https://msdn.microsoft.com/d71f3661-0efb-4376-966c-fb5c340ce1c5">BLOB</a> structures. The following values for 
<b>BTH_SET_SERVICE</b> members must be used.

For more information about class of device (COD), see the Bluetooth specification at 
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84017">www.bluetooth.com</a>.<table>
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
<a href="https://msdn.microsoft.com/3892bd59-97ac-4b76-bff9-7329f22a66cc">getsockname</a> function call.

Bluetooth implements a one-to-one correlation between SDP records and server sockets. As such, there is no need for the <b>SERVICE_MULTIPLE</b> flag.




## -see-also




<a href="https://msdn.microsoft.com/3892bd59-97ac-4b76-bff9-7329f22a66cc">Bluetooth
		  and getsockname</a>



<a href="https://msdn.microsoft.com/d71f3661-0efb-4376-966c-fb5c340ce1c5">Bluetooth and
		  BLOB</a>



<a href="https://msdn.microsoft.com/71c5ed9c-fade-4d15-848e-eb810ad4cbb2">Bluetooth and WSASetService</a>



<a href="https://msdn.microsoft.com/c52a7e7d-92ab-4103-a6c6-57c3fafec706">WSAQUERYSET</a>
 

 

