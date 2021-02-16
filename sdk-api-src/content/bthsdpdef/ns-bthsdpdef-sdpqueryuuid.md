---
UID: NS:bthsdpdef._SdpQueryUuid
title: SdpQueryUuid (bthsdpdef.h)
description: The SdpQueryUuid structure facilitates searching for UUIDs.
helpviewer_keywords: ["SdpQueryUuid","SdpQueryUuid structure [Bluetooth]","bluetooth.sdpqueryuuid","bthsdpdef/SdpQueryUuid"]
old-location: bluetooth\sdpqueryuuid.htm
tech.root: bluetooth
ms.assetid: 8c67b1b1-d289-4273-a512-589b19cd1f85
ms.date: 12/05/2018
ms.keywords: SdpQueryUuid, SdpQueryUuid structure [Bluetooth], bluetooth.sdpqueryuuid, bthsdpdef/SdpQueryUuid
req.header: bthsdpdef.h
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
req.typenames: SdpQueryUuid
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SdpQueryUuid
 - bthsdpdef/_SdpQueryUuid
 - SdpQueryUuid
 - bthsdpdef/SdpQueryUuid
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bthsdpdef.h
api_name:
 - SdpQueryUuid
---

# SdpQueryUuid structure


## -description

The <b>SdpQueryUuid</b> structure facilitates searching for UUIDs.

## -struct-fields

### -field u

Union containing the UUID on which to search.



### -field uuidType

Type of UUID being searched. Must be one of the three valid values from the SDP_SPECIFICTYPE enumeration:


<ul>
<li>SDP_ST_UUID16 - indicates u.uuid16 will be used in the search.</li>
<li>SDP_ST_UUID32 - indicates u.uuid32 will be used in the search.</li>
<li>SDP_ST_UUID128 - indicates u.uuid128 will be used in the search.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/ws2bth/ns-ws2bth-bth_query_service">BTH_QUERY_SERVICE</a>