---
UID: NF:mfapi.PackRatio
title: PackRatio function (mfapi.h)
description: Packs two UINT32 values, which represent a ratio, into a UINT64 value.
helpviewer_keywords: ["PackRatio","PackRatio function [Media Foundation]","mf.packratio","mfapi/PackRatio"]
old-location: mf\packratio.htm
tech.root: mf
ms.assetid: 2E175E21-D5A3-43B1-8AB9-A427E0F9350E
ms.date: 12/05/2018
ms.keywords: PackRatio, PackRatio function [Media Foundation], mf.packratio, mfapi/PackRatio
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
 - PackRatio
 - mfapi/PackRatio
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
 - PackRatio
---

# PackRatio function


## -description

Packs two UINT32 values, which represent a ratio, into a UINT64 value.

## -parameters

### -param nNumerator [in]

Value to store the <b>UINT32</b> numerator value.

### -param unDenominator [in]

Value to store the <b>UINT32</b> denominator value.

## -returns

Returns the packed <b>UINT64</b> value.

## -remarks

This function stores two 32-bit values in a 64-bit value that is suitable for the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64">IMFAttributes::SetUINT64</a> method.

## -see-also

<a href="/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio">MFGetAttributeRatio</a>



<a href="/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize">MFGetAttributeSize</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>