---
UID: NS:strmif.REGFILTER2
title: REGFILTER2 (strmif.h)
description: The REGFILTER2 structure contains information for registering a filter.
helpviewer_keywords: ["REGFILTER2","REGFILTER2 structure [DirectShow]","REGFILTER2Structure","dshow.regfilter2","strmif/REGFILTER2"]
old-location: dshow\regfilter2.htm
tech.root: dshow
ms.assetid: 651b94e6-b343-4957-9781-768b04c098dd
ms.date: 12/05/2018
ms.keywords: REGFILTER2, REGFILTER2 structure [DirectShow], REGFILTER2Structure, dshow.regfilter2, strmif/REGFILTER2
req.header: strmif.h
req.include-header: Dshow.h
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
req.typenames: REGFILTER2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - REGFILTER2
 - strmif/REGFILTER2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - REGFILTER2
---

# REGFILTER2 structure


## -description

The <code>REGFILTER2</code> structure contains information for registering a filter.

## -struct-fields

### -field dwVersion

Filter registration format. If the value is 1, the union contains the first unnamed structure. If the value is 2, the union contains the second unnamed structure.

### -field dwMerit

Filter merit. Filters with higher merit are enumerated first. See <a href="/windows/desktop/DirectShow/merit">Merit</a>.

### -field cPins

Number of pins. (Defined only if <b>dwVersion</b> is 1.)

### -field rgPins

Pointer to an array of <a href="/windows/desktop/api/strmif/ns-strmif-regfilterpins">REGFILTERPINS</a> structures, of size <b>cPins</b>. (Defined only if <b>dwVersion</b> is 1.)

### -field cPins2

Number of pins. (Defined only if <b>dwVersion</b> is 2.)

### -field rgPins2

Pointer to an array of <a href="/windows/desktop/api/strmif/ns-strmif-regfilterpins2">REGFILTERPINS2</a> structures, of size <b>cPins2</b>. (Defined only if <b>dwVersion</b> is 2.)

## -remarks

This structure is passed to the <a href="/windows/desktop/api/strmif/nf-strmif-ifiltermapper2-registerfilter">IFilterMapper2::RegisterFilter</a> method.

If you need to register pin mediums or pin categories, set <b>dwVersion</b> to 2 and use the <a href="/windows/desktop/api/strmif/ns-strmif-regfilterpins2">REGFILTERPINS2</a> structure.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>