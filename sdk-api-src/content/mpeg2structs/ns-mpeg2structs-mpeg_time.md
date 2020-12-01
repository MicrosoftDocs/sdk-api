---
UID: NS:mpeg2structs.__MIDL___MIDL_itf_mpeg2structs_0000_0000_0024
title: MPEG_TIME (mpeg2structs.h)
description: The MPEG_TIME structure represents a time of day, or a duration.
helpviewer_keywords: ["MPEG_DURATION","MPEG_TIME","MPEG_TIME structure [Microsoft TV Technologies]","mpeg2structs/MPEG_TIME","mstv.mpeg_time"]
old-location: mstv\mpeg_time.htm
tech.root: mstv
ms.assetid: b0a28edb-fcd8-43b4-a65c-d45e8a0f02b3
ms.date: 12/05/2018
ms.keywords: MPEG_DURATION, MPEG_TIME, MPEG_TIME structure [Microsoft TV Technologies], mpeg2structs/MPEG_TIME, mstv.mpeg_time
req.header: mpeg2structs.h
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
req.typenames: MPEG_TIME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_mpeg2structs_0000_0000_0024
 - mpeg2structs/__MIDL___MIDL_itf_mpeg2structs_0000_0000_0024
 - MPEG_TIME
 - mpeg2structs/MPEG_TIME
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mpeg2Structs.h
api_name:
 - MPEG_TIME
---

# MPEG_TIME structure


## -description

The <b>MPEG_TIME</b> structure represents a time of day, or a duration.

## -struct-fields

### -field Hours

Specifies the hours. The value can range from 0 to 23, inclusive.

### -field Minutes

Specifies the minutes. The value can range from 0 to 59, inclusive.

### -field Seconds

Specifies the seconds. The value can range from 0 to 59, inclusive.

## -remarks

The <b>MPEG_DURATION</b> structure is a <code>typedef</code> for the <b>MPEG_TIME</b> structure.

<pre class="syntax" xml:space="preserve"><code>typedef MPEG_TIME MPEG_DURATION;</code></pre>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-structures">BDA Structures</a>