---
UID: NE:codecapi.eAVEncMPVScanPattern
title: eAVEncMPVScanPattern (codecapi.h)
description: Specifies the macroblock scan pattern. This enumeration is used with the AVEncMPVScanPattern property.
helpviewer_keywords: ["codecapi/eAVEncMPVScanPattern","codecapi/eAVEncMPVScanPattern_AlternateScan","codecapi/eAVEncMPVScanPattern_Auto","codecapi/eAVEncMPVScanPattern_ZigZagScan","dshow.eavencmpvscanpattern","eAVEncMPVScanPattern","eAVEncMPVScanPattern enumeration [DirectShow]","eAVEncMPVScanPatternEnumeration","eAVEncMPVScanPattern_AlternateScan","eAVEncMPVScanPattern_Auto","eAVEncMPVScanPattern_ZigZagScan"]
old-location: dshow\eavencmpvscanpattern.htm
tech.root: dshow
ms.assetid: 8204705e-b944-4479-b8c8-d64ab9a4d5f2
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncMPVScanPattern, codecapi/eAVEncMPVScanPattern_AlternateScan, codecapi/eAVEncMPVScanPattern_Auto, codecapi/eAVEncMPVScanPattern_ZigZagScan, dshow.eavencmpvscanpattern, eAVEncMPVScanPattern, eAVEncMPVScanPattern enumeration [DirectShow], eAVEncMPVScanPatternEnumeration, eAVEncMPVScanPattern_AlternateScan, eAVEncMPVScanPattern_Auto, eAVEncMPVScanPattern_ZigZagScan
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
 - eAVEncMPVScanPattern
 - codecapi/eAVEncMPVScanPattern
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
 - eAVEncMPVScanPattern
---

# eAVEncMPVScanPattern enumeration


## -description

Specifies the macroblock scan pattern. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencmpvscanpattern-property">AVEncMPVScanPattern</a> property.

## -enum-fields

### -field eAVEncMPVScanPattern_Auto:0

The encoder selects the scan pattern.

### -field eAVEncMPVScanPattern_ZigZagScan:1

Zig-zag scan.

### -field eAVEncMPVScanPattern_AlternateScan:2

Alternate-vertical scan.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
