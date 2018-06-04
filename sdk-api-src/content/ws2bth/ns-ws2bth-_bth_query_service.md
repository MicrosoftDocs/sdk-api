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

# _BTH_QUERY_SERVICE structure


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
<a href="Http://go.microsoft.com/fwlink/p/?linkid=84017">www.bluetooth.com</a> for more information about the Bluetooth specification.




## -see-also




<a href="https://msdn.microsoft.com/d9961600-cdca-42ec-92eb-118b8186ed2e">Bluetooth and WSALookupServiceBegin for Service
		  Discovery</a>



<a href="https://msdn.microsoft.com/c52a7e7d-92ab-4103-a6c6-57c3fafec706">Bluetooth and WSAQUERYSET for Service Inquiry</a>
 

 

