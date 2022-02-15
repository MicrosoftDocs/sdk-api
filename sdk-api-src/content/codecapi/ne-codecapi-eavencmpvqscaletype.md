---
UID: NE:codecapi.eAVEncMPVQScaleType
title: eAVEncMPVQScaleType (codecapi.h)
description: Specifies whether the quantizer scale is linear or non-linear. This enumeration is used with the AVEncMPVQScaleType property.
helpviewer_keywords: ["codecapi/eAVEncMPVQScaleType","codecapi/eAVEncMPVQScaleType_Auto","codecapi/eAVEncMPVQScaleType_Linear","codecapi/eAVEncMPVScanPattern_AlternateScan","dshow.eavencmpvqscaletype","eAVEncMPVQScaleType","eAVEncMPVQScaleType enumeration [DirectShow]","eAVEncMPVQScaleTypeEnumeration","eAVEncMPVQScaleType_Auto","eAVEncMPVQScaleType_Linear","eAVEncMPVScanPattern_AlternateScan"]
old-location: dshow\eavencmpvqscaletype.htm
tech.root: dshow
ms.assetid: cc36ac03-66cb-4855-acf5-5f67265376b7
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncMPVQScaleType, codecapi/eAVEncMPVQScaleType_Auto, codecapi/eAVEncMPVQScaleType_Linear, codecapi/eAVEncMPVScanPattern_AlternateScan, dshow.eavencmpvqscaletype, eAVEncMPVQScaleType, eAVEncMPVQScaleType enumeration [DirectShow], eAVEncMPVQScaleTypeEnumeration, eAVEncMPVQScaleType_Auto, eAVEncMPVQScaleType_Linear, eAVEncMPVScanPattern_AlternateScan
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
 - eAVEncMPVQScaleType
 - codecapi/eAVEncMPVQScaleType
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
 - eAVEncMPVQScaleType
---

## -description

Specifies whether the quantizer scale is linear or non-linear. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencmpvqscaletype-property">AVEncMPVQScaleType</a> property.

## -enum-fields

### -field eAVEncMPVQScaleType_Auto:0

The encoder selects the quantization scale.

### -field eAVEncMPVQScaleType_Linear:1

The quantization scale is linear.

### -field eAVEncMPVQScaleType_NonLinear:2

The quantization scale is non-linear.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>

<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
