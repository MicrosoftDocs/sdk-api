---
UID: NE:codecapi.eAVEncMPVIntraVLCTable
title: eAVEncMPVIntraVLCTable (codecapi.h)
description: Specifies which variable-length coding (VLC) table to use for entropy coding. This enumeration is used with the AVEncMPVIntraVLCTable property.
helpviewer_keywords: ["codecapi/eAVEncMPVIntraVLCTable","codecapi/eAVEncMPVIntraVLCTable_Alternate","codecapi/eAVEncMPVIntraVLCTable_Auto","codecapi/eAVEncMPVIntraVLCTable_MPEG1","dshow.eavencmpvintravlctable","eAVEncMPVIntraVLCTable","eAVEncMPVIntraVLCTable enumeration [DirectShow]","eAVEncMPVIntraVLCTableEnumeration","eAVEncMPVIntraVLCTable_Alternate","eAVEncMPVIntraVLCTable_Auto","eAVEncMPVIntraVLCTable_MPEG1"]
old-location: dshow\eavencmpvintravlctable.htm
tech.root: dshow
ms.assetid: 132887a8-c1f6-47f2-9c8d-aa62560b0f8a
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncMPVIntraVLCTable, codecapi/eAVEncMPVIntraVLCTable_Alternate, codecapi/eAVEncMPVIntraVLCTable_Auto, codecapi/eAVEncMPVIntraVLCTable_MPEG1, dshow.eavencmpvintravlctable, eAVEncMPVIntraVLCTable, eAVEncMPVIntraVLCTable enumeration [DirectShow], eAVEncMPVIntraVLCTableEnumeration, eAVEncMPVIntraVLCTable_Alternate, eAVEncMPVIntraVLCTable_Auto, eAVEncMPVIntraVLCTable_MPEG1
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - eAVEncMPVIntraVLCTable
 - codecapi/eAVEncMPVIntraVLCTable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVEncMPVIntraVLCTable
---

# eAVEncMPVIntraVLCTable enumeration


## -description

Specifies which variable-length coding (VLC) table to use for entropy coding. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencmpvintravlctable-property">AVEncMPVIntraVLCTable</a> property.

## -enum-fields

### -field eAVEncMPVIntraVLCTable_Auto:0

The encoder selects the VLC table.

### -field eAVEncMPVIntraVLCTable_MPEG1:1

The encoder uses the MPEG-1 VLC table.

### -field eAVEncMPVIntraVLCTable_Alternate:2

The encoder uses the alternate "intra" VLC table for MPEG-2.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
