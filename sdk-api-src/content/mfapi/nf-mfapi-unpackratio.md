---
UID: NF:mfapi.UnpackRatio
title: UnpackRatio function (mfapi.h)
description: Gets the low-order and high-order UINT32 values from a UINT64 value that represents a ratio.
helpviewer_keywords: ["UnpackRatio","mf.unpackratio","mfapi/unpackratio","unpackratio","unpackratio function [Media Foundation]"]
old-location: mf\unpackratio.htm
tech.root: mf
ms.assetid: 8E4E1E6C-1C80-4A0B-98CE-2ED3443E1821
ms.date: 12/05/2018
ms.keywords: UnpackRatio, mf.unpackratio, mfapi/unpackratio, unpackratio, unpackratio function [Media Foundation]
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - UnpackRatio
 - mfapi/UnpackRatio
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - unpackratio
---

# UnpackRatio function


## -description

Gets the low-order and high-order <b>UINT32</b> values from a <b>UINT64</b> value that represents a ratio.

## -parameters

### -param unPacked [in]

The value to convert.

### -param pnNumerator [out]

Receives the high-order 32 bits.

### -param punDenominator [out]

Receives the low-order 32 bits.

## -remarks

You can use this function to unpack a <b>UINT64</b> value that you receive from the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64">IMFAttributes::GetUINT64</a> method.

## -see-also

<a href="/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio">MFGetAttributeRatio</a>



<a href="/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize">MFGetAttributeSize</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>