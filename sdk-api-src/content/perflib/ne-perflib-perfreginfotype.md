---
UID: NE:perflib._PerfRegInfoType
title: PerfRegInfoType (perflib.h)
description: Indicates the types of information that you can request about a performance counter set by calling the PerfQueryCounterSetRegistrationInfo function.
helpviewer_keywords: ["PERF_REG_COUNTERSET_ENGLISH_NAME","PERF_REG_COUNTERSET_HELP_STRING","PERF_REG_COUNTERSET_NAME_STRING","PERF_REG_COUNTERSET_STRUCT","PERF_REG_COUNTER_ENGLISH_NAMES","PERF_REG_COUNTER_HELP_STRINGS","PERF_REG_COUNTER_NAME_STRINGS","PERF_REG_COUNTER_STRUCT","PERF_REG_PROVIDER_GUID","PERF_REG_PROVIDER_NAME","PerfRegInfoType","PerfRegInfoType enumeration [Perf]","perf.perfreginfotype","perflib/PERF_REG_COUNTERSET_ENGLISH_NAME","perflib/PERF_REG_COUNTERSET_HELP_STRING","perflib/PERF_REG_COUNTERSET_NAME_STRING","perflib/PERF_REG_COUNTERSET_STRUCT","perflib/PERF_REG_COUNTER_ENGLISH_NAMES","perflib/PERF_REG_COUNTER_HELP_STRINGS","perflib/PERF_REG_COUNTER_NAME_STRINGS","perflib/PERF_REG_COUNTER_STRUCT","perflib/PERF_REG_PROVIDER_GUID","perflib/PERF_REG_PROVIDER_NAME","perflib/PerfRegInfoType"]
old-location: perf\perfreginfotype.htm
tech.root: perf
ms.assetid: 8D54F31F-9ABA-405F-84A5-9C7225B7BE67
ms.date: 12/05/2018
ms.keywords: PERF_REG_COUNTERSET_ENGLISH_NAME, PERF_REG_COUNTERSET_HELP_STRING, PERF_REG_COUNTERSET_NAME_STRING, PERF_REG_COUNTERSET_STRUCT, PERF_REG_COUNTER_ENGLISH_NAMES, PERF_REG_COUNTER_HELP_STRINGS, PERF_REG_COUNTER_NAME_STRINGS, PERF_REG_COUNTER_STRUCT, PERF_REG_PROVIDER_GUID, PERF_REG_PROVIDER_NAME, PerfRegInfoType, PerfRegInfoType enumeration [Perf], perf.perfreginfotype, perflib/PERF_REG_COUNTERSET_ENGLISH_NAME, perflib/PERF_REG_COUNTERSET_HELP_STRING, perflib/PERF_REG_COUNTERSET_NAME_STRING, perflib/PERF_REG_COUNTERSET_STRUCT, perflib/PERF_REG_COUNTER_ENGLISH_NAMES, perflib/PERF_REG_COUNTER_HELP_STRINGS, perflib/PERF_REG_COUNTER_NAME_STRINGS, perflib/PERF_REG_COUNTER_STRUCT, perflib/PERF_REG_PROVIDER_GUID, perflib/PERF_REG_PROVIDER_NAME, perflib/PerfRegInfoType
req.header: perflib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: PerfRegInfoType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PerfRegInfoType
 - perflib/_PerfRegInfoType
 - PerfRegInfoType
 - perflib/PerfRegInfoType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Perflib.h
api_name:
 - PerfRegInfoType
---

# PerfRegInfoType enumeration


## -description

Indicates the types of information that you can request about a performance counter set by calling the <a href="/windows/desktop/api/perflib/nf-perflib-perfquerycountersetregistrationinfo">PerfQueryCounterSetRegistrationInfo</a> function.

## -enum-fields

### -field PERF_REG_COUNTERSET_STRUCT:1

Gets the registration information for a counter set and all of the counters it contains as a <a href="/windows/desktop/api/perflib/ns-perflib-perf_counterset_reg_info">PERF_COUNTERSET_REG_INFO</a> block.  The block includes a <b>PERF_COUNTERSET_REG_INFO</b> structure followed by one or  

        more <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_reg_info">PERF_COUNTER_REG_INFO</a> structures.

### -field PERF_REG_COUNTER_STRUCT

Gets the registration information for a performance counter as  a <a href="/windows/desktop/api/perflib/ns-perflib-perf_counter_reg_info">PERF_COUNTER_REG_INFO</a> structure.  

        Use the <i>requestLangId</i> parameter of the <a href="/windows/desktop/api/perflib/nf-perflib-perfquerycountersetregistrationinfo">PerfQueryCounterSetRegistrationInfo</a> function to specify the counter identifier.

### -field PERF_REG_COUNTERSET_NAME_STRING

Gets a null-terminated UTF16-LE string that indicates the name of the counter set.  

        Use the <i>requestLangId</i> parameter of the <a href="/windows/desktop/api/perflib/nf-perflib-perfquerycountersetregistrationinfo">PerfQueryCounterSetRegistrationInfo</a> function  to specify the preferred locale of the result.

### -field PERF_REG_COUNTERSET_HELP_STRING

Gets a null-terminated UTF16-LE string that contains the help string for the counter set.  

        Use the <i>requestLangId</i> parameter of the <a href="/windows/desktop/api/perflib/nf-perflib-perfquerycountersetregistrationinfo">PerfQueryCounterSetRegistrationInfo</a> function to specify the preferred locale of the result.

### -field PERF_REG_COUNTER_NAME_STRINGS

   Gets the names of the performance counters in the counter set as a <a href="/windows/win32/api/perflib/ns-perflib-perf_string_buffer_header">PERF_STRING_BUFFER_HEADER</a> block.  

        The block includes a <b>PERF_STRING_BUFFER_HEADER</b> structure, followed by one  

        or more <a href="/windows/win32/api/perflib/ns-perflib-perf_string_counter_header">PERF_STRING_COUNTER_HEADER</a> structures, followed by string data that indicates the counter names.  

        Use the <i>requestLangId</i> parameter of the <a href="/windows/desktop/api/perflib/nf-perflib-perfquerycountersetregistrationinfo">PerfQueryCounterSetRegistrationInfo</a> function to specify the preferred locale of the result.

### -field PERF_REG_COUNTER_HELP_STRINGS

Gets the help  strings for the performance counters in the counter set as a <a href="/windows/win32/api/perflib/ns-perflib-perf_string_buffer_header">PERF_STRING_BUFFER_HEADER</a> block.  

        The block includes a <b>PERF_STRING_BUFFER_HEADER</b> structure, followed by one  

        or more <a href="/windows/win32/api/perflib/ns-perflib-perf_string_counter_header">PERF_STRING_COUNTER_HEADER</a> structures, followed by string data that contains the help strings.  

        Use the <i>requestLangId</i> parameter of the <a href="/windows/desktop/api/perflib/nf-perflib-perfquerycountersetregistrationinfo">PerfQueryCounterSetRegistrationInfo</a> function to specify the preferred locale of the result.

### -field PERF_REG_PROVIDER_NAME

Gets a null-terminated UTF-16LE string that indicates the name of the provider for the counter set.

### -field PERF_REG_PROVIDER_GUID

Gets the GUID of the provider for the counter set.

### -field PERF_REG_COUNTERSET_ENGLISH_NAME

Gets a null-terminated UTF-16LE string that contains the name of the counter set in English. This value is equivalent to setting the <i>requestCode</i> parameter to <b>PERF_REG_COUNTERSET_NAME_STRING</b> and the  <i>requestLangId</i> parameter to 0 when you call the <a href="/windows/desktop/api/perflib/nf-perflib-perfquerycountersetregistrationinfo">PerfQueryCounterSetRegistrationInfo</a> function.

### -field PERF_REG_COUNTER_ENGLISH_NAMES

Gets the English  names of the performance counters in the counter set as a <a href="/windows/win32/api/perflib/ns-perflib-perf_string_buffer_header">PERF_STRING_BUFFER_HEADER</a> block.  

        The block includes a <b>PERF_STRING_BUFFER_HEADER</b> structure, followed by one  

        or more <a href="/windows/win32/api/perflib/ns-perflib-perf_string_counter_header">PERF_STRING_COUNTER_HEADER</a> structures, followed by string data that indicates the counter names. This value is equivalent to setting the <i>requestCode</i> parameter to  <b>PERF_REG_COUNTER_NAME_STRINGS</b>  and the  <i>requestLangId</i> parameter to 0 when you call the <a href="/windows/desktop/api/perflib/nf-perflib-perfquerycountersetregistrationinfo">PerfQueryCounterSetRegistrationInfo</a> function.

## -see-also

<a href="/windows/desktop/api/perflib/nf-perflib-perfquerycountersetregistrationinfo">PerfQueryCounterSetRegistrationInfo</a>
