---
UID: NE:tapi3if.FULLDUPLEX_SUPPORT
title: FULLDUPLEX_SUPPORT (tapi3if.h)
description: The FULLDUPLEX_SUPPORT enum is used by applications interacting with legacy TSPs to indicate whether a specified terminal supports full duplex operations. This enum is returned by the ITLegacyWaveSupport::IsFullDuplex method.
helpviewer_keywords: ["FDS_NOTSUPPORTED","FDS_SUPPORTED","FDS_UNKNOWN","FULLDUPLEX_SUPPORT","FULLDUPLEX_SUPPORT enumeration [TAPI 2.2]","_tapi3_fullduplex_support","tapi3.fullduplex_support","tapi3if/FDS_NOTSUPPORTED","tapi3if/FDS_SUPPORTED","tapi3if/FDS_UNKNOWN","tapi3if/FULLDUPLEX_SUPPORT"]
old-location: tapi3\fullduplex_support.htm
tech.root: tapi3
ms.assetid: 36f9f126-361f-448a-a464-ffef1de25d26
ms.date: 12/05/2018
ms.keywords: FDS_NOTSUPPORTED, FDS_SUPPORTED, FDS_UNKNOWN, FULLDUPLEX_SUPPORT, FULLDUPLEX_SUPPORT enumeration [TAPI 2.2], _tapi3_fullduplex_support, tapi3.fullduplex_support, tapi3if/FDS_NOTSUPPORTED, tapi3if/FDS_SUPPORTED, tapi3if/FDS_UNKNOWN, tapi3if/FULLDUPLEX_SUPPORT
req.header: tapi3if.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FULLDUPLEX_SUPPORT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FULLDUPLEX_SUPPORT
 - tapi3if/FULLDUPLEX_SUPPORT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - FULLDUPLEX_SUPPORT
---

# FULLDUPLEX_SUPPORT enumeration


## -description

The 
<b>FULLDUPLEX_SUPPORT</b> enum is used by applications interacting with legacy TSPs to indicate whether a specified terminal supports full duplex operations. This enum is returned by the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacywavesupport-isfullduplex">ITLegacyWaveSupport::IsFullDuplex</a> method.

## -enum-fields

### -field FDS_SUPPORTED:0

Full duplex supported.

### -field FDS_NOTSUPPORTED

Full duplex not supported.

### -field FDS_UNKNOWN

The TSP cannot determine whether the device is full duplex.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacywavesupport-isfullduplex">ITLegacyWaveSupport::IsFullDuplex</a>
