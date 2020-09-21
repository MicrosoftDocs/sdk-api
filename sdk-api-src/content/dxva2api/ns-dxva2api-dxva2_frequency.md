---
UID: NS:dxva2api._DXVA2_Frequency
title: DXVA2_Frequency (dxva2api.h)
description: Defines a video frequency.
helpviewer_keywords: ["03b6bef9-c0ba-4efa-9552-55c8e9fd77ae","DXVA2_Frequency","DXVA2_Frequency structure [Media Foundation]","dxva2api/DXVA2_Frequency","mf.dxva2_frequency"]
old-location: mf\dxva2_frequency.htm
tech.root: mf
ms.assetid: 03b6bef9-c0ba-4efa-9552-55c8e9fd77ae
ms.date: 12/05/2018
ms.keywords: 03b6bef9-c0ba-4efa-9552-55c8e9fd77ae, DXVA2_Frequency, DXVA2_Frequency structure [Media Foundation], dxva2api/DXVA2_Frequency, mf.dxva2_frequency
req.header: dxva2api.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: DXVA2_Frequency
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVA2_Frequency
 - dxva2api/_DXVA2_Frequency
 - DXVA2_Frequency
 - dxva2api/DXVA2_Frequency
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxva2api.h
api_name:
 - DXVA2_Frequency
---

# DXVA2_Frequency structure


## -description

Defines a video frequency.

## -struct-fields

### -field Numerator

Numerator of the frequency.

### -field Denominator

Denominator of the frequency.

## -remarks

The value 0/0 indicates an unknown frequency. Values of the form <i>n</i>/0, where <i>n</i> is not zero, are invalid. Values of the form 0/<i>n</i>, where <i>n</i> is not zero, indicate a frequency of zero.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>