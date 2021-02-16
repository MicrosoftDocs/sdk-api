---
UID: NS:ws2bth._BTH_QUERY_SERVICE
title: BTH_QUERY_SERVICE (ws2bth.h)
description: The BTH_QUERY_SERVICE structure is used to query a Bluetooth service.
helpviewer_keywords: ["*PBTHNS_RESTRICTIONBLOB","*PBTH_QUERY_SERVICE","BTHNS_RESTRICTIONBLOB","BTH_QUERY_SERVICE","BTH_QUERY_SERVICE structure [Bluetooth]","PBTH_QUERY_SERVICE","PBTH_QUERY_SERVICE structure pointer [Bluetooth]","_bth_bth_query_service","bluetooth.bth_query_service","ws2bth/BTH_QUERY_SERVICE","ws2bth/PBTH_QUERY_SERVICE"]
old-location: bluetooth\bth_query_service.htm
tech.root: bluetooth
ms.assetid: b208b7d6-305c-4acc-9c89-75721ff5dcb2
ms.date: 12/05/2018
ms.keywords: '*PBTHNS_RESTRICTIONBLOB, *PBTH_QUERY_SERVICE, BTHNS_RESTRICTIONBLOB, BTH_QUERY_SERVICE, BTH_QUERY_SERVICE structure [Bluetooth], PBTH_QUERY_SERVICE, PBTH_QUERY_SERVICE structure pointer [Bluetooth], _bth_bth_query_service, bluetooth.bth_query_service, ws2bth/BTH_QUERY_SERVICE, ws2bth/PBTH_QUERY_SERVICE'
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
req.typenames: BTH_QUERY_SERVICE, *PBTH_QUERY_SERVICE, BTHNS_RESTRICTIONBLOB, *PBTHNS_RESTRICTIONBLOB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BTH_QUERY_SERVICE
 - ws2bth/_BTH_QUERY_SERVICE
 - PBTH_QUERY_SERVICE
 - ws2bth/PBTH_QUERY_SERVICE
 - BTH_QUERY_SERVICE
 - ws2bth/BTH_QUERY_SERVICE
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
 - BTH_QUERY_SERVICE
---

# BTH_QUERY_SERVICE structure


## -description

The 
<b>BTH_QUERY_SERVICE</b> structure is used to query a Bluetooth service.

## -struct-fields

### -field type

Type of service to perform. Choose from the following:

<ul>
<li>SDP_SERVICE_SEARCH_REQUEST</li>
<li>SDP_SERVICE_ATTRIBUTE_REQUEST</li>
<li>SDP_SERVICE_SEARCH_ATTRIBUTE_REQUEST</li>
</ul>

### -field serviceHandle

Service handle on which to query the attributes specified in the <b>pRange</b> member. Used only for attribute searches.

### -field uuids

UUIDs that a record must contain to match the search. Used for service and service attribute searches. When querying less than MAX_UUIDS_IN_QUERY UUIDs, set the <b>SdpQueryUuid</b> element immediately following the last valid UUID to all zeros. Used only for attribute and service attribute searches.

### -field numRange

Number of elements in <b>pRange</b>. Used only for attribute and service attribute searches.

### -field pRange

Attribute values to retrieve for any matching records, in the form of an array of 
<b>SdpAttributeRange</b> structures. Attributes are defined in the Bluetooth specification. See Remarks.

## -remarks

The <b>pRange</b> member is an open-ended array specifying a sparse set of attributes to return from the query. It is an application's responsibility to provide a nonoverlapping array that is sorted in ascending order of attribute ID, without duplicates.

See 
<a href="https://www.bluetooth.com/">www.bluetooth.com</a> for more information about the Bluetooth specification.

## -see-also

<a href="/windows/desktop/Bluetooth/bluetooth-and-wsalookupservicebegin-for-service-discovery">Bluetooth and WSALookupServiceBegin for Service
		  Discovery</a>



<a href="/windows/desktop/Bluetooth/bluetooth-and-wsaqueryset-for-service-inquiry">Bluetooth and WSAQUERYSET for Service Inquiry</a>