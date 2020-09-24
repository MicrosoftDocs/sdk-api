---
UID: NS:timeprov.TpcGetSamplesArgs
title: TpcGetSamplesArgs (timeprov.h)
description: A structure that is used by the TimeProvCommand function.
helpviewer_keywords: ["TpcGetSamplesArgs","TpcGetSamplesArgs structure","_win32_tpcgetsamplesargs_str","base.tpcgetsamplesargs_str","timeprov/TpcGetSamplesArgs"]
old-location: base\tpcgetsamplesargs_str.htm
tech.root: winprog
ms.assetid: 7e92a7c1-6927-4d53-8252-6bdd424d6e0c
ms.date: 12/05/2018
ms.keywords: TpcGetSamplesArgs, TpcGetSamplesArgs structure, _win32_tpcgetsamplesargs_str, base.tpcgetsamplesargs_str, timeprov/TpcGetSamplesArgs
req.header: timeprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: TpcGetSamplesArgs
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TpcGetSamplesArgs
 - timeprov/TpcGetSamplesArgs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Timeprov.h
api_name:
 - TpcGetSamplesArgs
---

# TpcGetSamplesArgs structure


## -description

A structure that is used by the 
<a href="/windows/desktop/api/timeprov/nf-timeprov-timeprovcommand">TimeProvCommand</a> function.

## -struct-fields

### -field pbSampleBuf

An array of 
<a href="/windows/desktop/api/timeprov/ns-timeprov-timesample">TimeSample</a> structures.

### -field cbSampleBuf

The size of <b>pbSampleBuf</b>, in bytes.

### -field dwSamplesReturned

The number of samples returned.

### -field dwSamplesAvailable

The total number of samples available.

## -see-also

<a href="/windows/desktop/api/timeprov/nf-timeprov-timeprovcommand">TimeProvCommand</a>



<a href="/windows/desktop/api/timeprov/ns-timeprov-timesample">TimeSample</a>