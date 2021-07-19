---
UID: NS:bthsdpdef.SdpAttributeRange
title: SdpAttributeRange (bthsdpdef.h)
description: The SdpAttributeRange structure is used in a Bluetooth query to constrain the set of attributes to return in the query.
helpviewer_keywords: ["SdpAttributeRange","SdpAttributeRange structure [Bluetooth]","bluetooth.sdpattributerange","bthsdpdef/SdpAttributeRange"]
old-location: bluetooth\sdpattributerange.htm
tech.root: bluetooth
ms.assetid: 2b8bf753-a3c4-4a41-89c7-0caac76cfd33
ms.date: 12/05/2018
ms.keywords: SdpAttributeRange, SdpAttributeRange structure [Bluetooth], bluetooth.sdpattributerange, bthsdpdef/SdpAttributeRange
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
req.typenames: SdpAttributeRange
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SdpAttributeRange
 - bthsdpdef/_SdpAttributeRange
 - SdpAttributeRange
 - bthsdpdef/SdpAttributeRange
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
 - SdpAttributeRange
---

# SdpAttributeRange structure


## -description

The <b>SdpAttributeRange</b> structure is used in a Bluetooth query to constrain the set of attributes to return in the query.

## -struct-fields

### -field minAttribute

Minimum attribute value for which to search.

### -field maxAttribute

Maximum attribute value for which to search.

## -see-also

<a href="/windows/desktop/api/ws2bth/ns-ws2bth-bth_query_service">BTH_QUERY_SERVICE</a>