---
UID: NF:mfapi.Unpack2UINT32AsUINT64
title: Unpack2UINT32AsUINT64 function (mfapi.h)
description: Gets the low-order and high-order UINT32 values from a UINT64 value.
helpviewer_keywords: ["Unpack2UINT32AsUINT64","Unpack2UINT32AsUINT64 function [Media Foundation]","mf.unpack2uint32asuint64","mfapi/Unpack2UINT32AsUINT64"]
old-location: mf\unpack2uint32asuint64.htm
tech.root: mf
ms.assetid: 507504c2-85d3-44b6-9972-bcdd3c4227f6
ms.date: 12/05/2018
ms.keywords: Unpack2UINT32AsUINT64, Unpack2UINT32AsUINT64 function [Media Foundation], mf.unpack2uint32asuint64, mfapi/Unpack2UINT32AsUINT64
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - Unpack2UINT32AsUINT64
 - mfapi/Unpack2UINT32AsUINT64
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
 - Unpack2UINT32AsUINT64
---

# Unpack2UINT32AsUINT64 function


## -description

Gets the low-order and high-order <b>UINT32</b> values from a <b>UINT64</b> value.

## -parameters

### -param unPacked [in]

The value to convert.

### -param punHigh [out]

Receives the high-order 32 bits.

### -param punLow [out]

Receives the low-order 32 bits.

## -remarks

You can use this function to unpack a <b>UINT64</b> value that you receive from the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64">IMFAttributes::GetUINT64</a> method.

## -see-also

<a href="/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio">MFGetAttributeRatio</a>



<a href="/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize">MFGetAttributeSize</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>