---
UID: NE:codecapi.eAVEncDDSurroundExMode
title: eAVEncDDSurroundExMode (codecapi.h)
description: Specifies whether a Dolby Digital audio stream is encoded in Dolby Digital Surround EX. This enumeration is used with the AVEncDDSurroundExMode property.
helpviewer_keywords: ["codecapi/eAVEncDDSurroundExMode","codecapi/eAVEncDDSurroundExMode_No","codecapi/eAVEncDDSurroundExMode_NotIndicated","codecapi/eAVEncDDSurroundExMode_Yes","dshow.eavencddsurroundexmode","eAVEncDDSurroundExMode","eAVEncDDSurroundExMode enumeration [DirectShow]","eAVEncDDSurroundExModeEnumeration","eAVEncDDSurroundExMode_No","eAVEncDDSurroundExMode_NotIndicated","eAVEncDDSurroundExMode_Yes"]
old-location: dshow\eavencddsurroundexmode.htm
tech.root: dshow
ms.assetid: 067614ca-c32d-4160-ae77-4e6c3dbafdf0
ms.date: 12/05/2018
ms.keywords: codecapi/eAVEncDDSurroundExMode, codecapi/eAVEncDDSurroundExMode_No, codecapi/eAVEncDDSurroundExMode_NotIndicated, codecapi/eAVEncDDSurroundExMode_Yes, dshow.eavencddsurroundexmode, eAVEncDDSurroundExMode, eAVEncDDSurroundExMode enumeration [DirectShow], eAVEncDDSurroundExModeEnumeration, eAVEncDDSurroundExMode_No, eAVEncDDSurroundExMode_NotIndicated, eAVEncDDSurroundExMode_Yes
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
 - eAVEncDDSurroundExMode
 - codecapi/eAVEncDDSurroundExMode
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
 - eAVEncDDSurroundExMode
---

# eAVEncDDSurroundExMode enumeration


## -description

Specifies whether a Dolby Digital audio stream is encoded in Dolby Digital Surround EX. This enumeration is used with the <a href="/windows/desktop/DirectShow/avencddsurroundexmode-property">AVEncDDSurroundExMode</a> property.

## -enum-fields

### -field eAVEncDDSurroundExMode_NotIndicated:0

The Surround EX mode is not indicated.

### -field eAVEncDDSurroundExMode_No:1

The audio is not encoded in Surround EX.

### -field eAVEncDDSurroundExMode_Yes:2

The audio is encoded in Surround EX.

## -see-also

<a href="/windows/desktop/DirectShow/codec-api-enumerations">Codec API Enumerations</a>



<a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI Interface</a>
