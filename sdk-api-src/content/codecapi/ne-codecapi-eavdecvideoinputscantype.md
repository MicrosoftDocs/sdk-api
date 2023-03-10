---
UID: NE:codecapi.eAVDecVideoInputScanType
title: eAVDecVideoInputScanType (codecapi.h)
description: Specifies how the decoded video stream is interlaced. This enumeration is used with the AVDecVideoInputScanType property.
helpviewer_keywords: ["codecapi/eAVDecVideoInputScanType","codecapi/eAVDecVideoInputScan_Interlaced_LowerFieldFirst","codecapi/eAVDecVideoInputScan_Interlaced_UpperFieldFirst","codecapi/eAVDecVideoInputScan_Progressive","codecapi/eAVDecVideoInputScan_Unknown","dshow.eavdecvideoinputscantype","eAVDecVideoInputScanType","eAVDecVideoInputScanType enumeration [DirectShow]","eAVDecVideoInputScanTypeEnumeration","eAVDecVideoInputScan_Interlaced_LowerFieldFirst","eAVDecVideoInputScan_Interlaced_UpperFieldFirst","eAVDecVideoInputScan_Progressive","eAVDecVideoInputScan_Unknown"]
old-location: dshow\eavdecvideoinputscantype.htm
tech.root: dshow
ms.assetid: 9ea17960-af08-42ba-9646-7aaf498ceda1
ms.date: 12/05/2018
ms.keywords: codecapi/eAVDecVideoInputScanType, codecapi/eAVDecVideoInputScan_Interlaced_LowerFieldFirst, codecapi/eAVDecVideoInputScan_Interlaced_UpperFieldFirst, codecapi/eAVDecVideoInputScan_Progressive, codecapi/eAVDecVideoInputScan_Unknown, dshow.eavdecvideoinputscantype, eAVDecVideoInputScanType, eAVDecVideoInputScanType enumeration [DirectShow], eAVDecVideoInputScanTypeEnumeration, eAVDecVideoInputScan_Interlaced_LowerFieldFirst, eAVDecVideoInputScan_Interlaced_UpperFieldFirst, eAVDecVideoInputScan_Progressive, eAVDecVideoInputScan_Unknown
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
 - eAVDecVideoInputScanType
 - codecapi/eAVDecVideoInputScanType
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
 - eAVDecVideoInputScanType
---

# eAVDecVideoInputScanType enumeration


## -description

Specifies how the decoded video stream is interlaced. This enumeration is used with the <a href="/windows/desktop/DirectShow/avdecvideoinputscantype-property">AVDecVideoInputScanType</a> property.

## -enum-fields

### -field eAVDecVideoInputScan_Unknown:0

The interlacing is not known.

### -field eAVDecVideoInputScan_Progressive:1

Decoded frames are progressive.

### -field eAVDecVideoInputScan_Interlaced_UpperFieldFirst:2

Decoded frames are interlaced, with the upper field appearing first.

### -field eAVDecVideoInputScan_Interlaced_LowerFieldFirst:3

Decoded frames are interlaced, with the lower field appearing first.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
