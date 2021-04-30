---
UID: NS:bthsdpdef.SdpQueryUuidUnion
title: SdpQueryUuidUnion (bthsdpdef.h)
description: The SdpQueryUuidUnion union contains the UUID on which to perform an SDP query. Used in conjunction with the SdpQueryUuid structure.
helpviewer_keywords: ["SdpQueryUuidUnion","SdpQueryUuidUnion structure [Bluetooth]","bluetooth.sdpqueryuuidunion","bthsdpdef/SdpQueryUuidUnion"]
old-location: bluetooth\sdpqueryuuidunion.htm
tech.root: bluetooth
ms.assetid: 446b0337-ea83-4d8a-bee7-3cccf03e61a5
ms.date: 12/05/2018
ms.keywords: SdpQueryUuidUnion, SdpQueryUuidUnion structure [Bluetooth], bluetooth.sdpqueryuuidunion, bthsdpdef/SdpQueryUuidUnion
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
req.typenames: SdpQueryUuidUnion
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SdpQueryUuidUnion
 - bthsdpdef/SdpQueryUuidUnion
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
 - SdpQueryUuidUnion
---

# SdpQueryUuidUnion structure


## -description

The <b>SdpQueryUuidUnion</b> union contains the UUID on which to perform an SDP query. Used in conjunction with the <b>SdpQueryUuid</b> structure.

## -struct-fields

### -field uuid128

UUID in 128-bit format.

### -field uuid128.case

### -field uuid128.case.SDP_ST_UUID128

### -field uuid32

UUID in 32-bit format.

### -field uuid32.case

### -field uuid32.case.SDP_ST_UUID32

### -field uuid16

UUID in 16-bit format.

### -field uuid16.case

### -field uuid16.case.SDP_ST_UUID16



## -see-also

<a href="/windows/desktop/api/ws2bth/ns-ws2bth-bth_query_service">BTH_QUERY_SERVICE</a>



<a href="/windows/desktop/api/bthsdpdef/ns-bthsdpdef-sdpqueryuuid">SdpQueryUuid</a>