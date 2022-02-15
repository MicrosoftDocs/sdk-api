---
UID: NE:avrfsdk.eHeapEnumerationLevel
title: eHeapEnumerationLevel (avrfsdk.h)
description: Determines whether the enumeration operation should continue or stop.
helpviewer_keywords: ["HeapEnumerationEverything","HeapEnumerationStop","avrfsdk/HeapEnumerationEverything","avrfsdk/HeapEnumerationStop","avrfsdk/eHeapEnumerationLevel","base.eheapenumerationlevel","eHeapEnumerationLevel","eHeapEnumerationLevel enumeration [Windows API]","winprog.eheapenumerationlevel"]
old-location: winprog\eheapenumerationlevel.htm
tech.root: winprog
ms.assetid: f8260ae8-eb1e-45f4-babc-905f4af7e3b1
ms.date: 12/05/2018
ms.keywords: HeapEnumerationEverything, HeapEnumerationStop, avrfsdk/HeapEnumerationEverything, avrfsdk/HeapEnumerationStop, avrfsdk/eHeapEnumerationLevel, base.eheapenumerationlevel, eHeapEnumerationLevel, eHeapEnumerationLevel enumeration [Windows API], winprog.eheapenumerationlevel
req.header: avrfsdk.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - eHeapEnumerationLevel
 - avrfsdk/eHeapEnumerationLevel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Avrfsdk.h
api_name:
 - eHeapEnumerationLevel
---

# eHeapEnumerationLevel enumeration


## -description

Determines whether the enumeration operation should continue or stop.

## -enum-fields

### -field HeapEnumerationEverything:0x0

A constant that specifies the enumeration should continue.

### -field HeapEnumerationStop:0xFFFFFFFF

A constant that specifies to the <a href="/windows/desktop/api/avrfsdk/nf-avrfsdk-verifierenumerateresource">VerifierEnumerateResource</a> function when the enumeration operation should stop.

Codes from 0x1 to 0xFFFFFFE are reserved.

## -see-also

<a href="/windows/desktop/DevNotes/resource-enumeration">Resource Enumeration</a>



<a href="/windows/desktop/api/avrfsdk/nf-avrfsdk-verifierenumerateresource">VerifierEnumerateResource</a>
