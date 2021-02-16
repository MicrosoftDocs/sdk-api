---
UID: NS:avrfsdk._AVRF_BACKTRACE_INFORMATION
title: AVRF_BACKTRACE_INFORMATION (avrfsdk.h)
description: Contains information about backtraces performed.
helpviewer_keywords: ["*PAVRF_BACKTRACE_INFORMATION","AVRF_BACKTRACE_INFORMATION","AVRF_BACKTRACE_INFORMATION structure [Windows API]","avrfsdk/AVRF_BACKTRACE_INFORMATION","base.avrf_backtrace_information","winprog.avrf_backtrace_information"]
old-location: winprog\avrf_backtrace_information.htm
tech.root: winprog
ms.assetid: 634d9569-469c-4dc7-9192-217af0937b6c
ms.date: 12/05/2018
ms.keywords: '*PAVRF_BACKTRACE_INFORMATION, AVRF_BACKTRACE_INFORMATION, AVRF_BACKTRACE_INFORMATION structure [Windows API], avrfsdk/AVRF_BACKTRACE_INFORMATION, base.avrf_backtrace_information, winprog.avrf_backtrace_information'
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
req.typenames: AVRF_BACKTRACE_INFORMATION, *PAVRF_BACKTRACE_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AVRF_BACKTRACE_INFORMATION
 - avrfsdk/_AVRF_BACKTRACE_INFORMATION
 - PAVRF_BACKTRACE_INFORMATION
 - avrfsdk/PAVRF_BACKTRACE_INFORMATION
 - AVRF_BACKTRACE_INFORMATION
 - avrfsdk/AVRF_BACKTRACE_INFORMATION
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
 - AVRF_BACKTRACE_INFORMATION
---

# AVRF_BACKTRACE_INFORMATION structure


## -description

Contains information about backtraces performed.

## -struct-fields

### -field Depth

The number of traces that have been collected.

### -field Index

A unique identifier associated with the entire set of returned addresses.

### -field ReturnAddresses

An array of addresses returned traces. The number cannot exceed AVRF_MAX_TRACES, which is defined as 32.

## -see-also

<a href="/windows/desktop/DevNotes/resource-enumeration">Resource Enumeration</a>



<a href="/windows/desktop/api/avrfsdk/nf-avrfsdk-verifierenumerateresource">VerifierEnumerateResource</a>