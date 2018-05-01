---
UID: NE:perflib._PerfRegInfoType
title: "_PerfRegInfoType"
author: windows-driver-content
description: Indicates the types of information that you can request about a performance counter set by calling the PerfQueryCounterSetRegistrationInfo function.
old-location: perf\perfreginfotype.htm
old-project: PerfCtrs
ms.assetid: 8D54F31F-9ABA-405F-84A5-9C7225B7BE67
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: PERF_REG_COUNTERSET_ENGLISH_NAME, PERF_REG_COUNTERSET_HELP_STRING, PERF_REG_COUNTERSET_NAME_STRING, PERF_REG_COUNTERSET_STRUCT, PERF_REG_COUNTER_ENGLISH_NAMES, PERF_REG_COUNTER_HELP_STRINGS, PERF_REG_COUNTER_NAME_STRINGS, PERF_REG_COUNTER_STRUCT, PERF_REG_PROVIDER_GUID, PERF_REG_PROVIDER_NAME, PerfRegInfoType, PerfRegInfoType enumeration [Perf], _PerfRegInfoType, perf.perfreginfotype, perflib/PERF_REG_COUNTERSET_ENGLISH_NAME, perflib/PERF_REG_COUNTERSET_HELP_STRING, perflib/PERF_REG_COUNTERSET_NAME_STRING, perflib/PERF_REG_COUNTERSET_STRUCT, perflib/PERF_REG_COUNTER_ENGLISH_NAMES, perflib/PERF_REG_COUNTER_HELP_STRINGS, perflib/PERF_REG_COUNTER_NAME_STRINGS, perflib/PERF_REG_COUNTER_STRUCT, perflib/PERF_REG_PROVIDER_GUID, perflib/PERF_REG_PROVIDER_NAME, perflib/PerfRegInfoType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: PerfRegInfoType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Perflib.h
api_name:
-	PerfRegInfoType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _PerfRegInfoType enumeration


## -description


Indicates the types of information that you can request about a performance counter set by calling the <a href="https://msdn.microsoft.com/E8E83E47-2445-42AE-855F-6710FC8F789E">PerfQueryCounterSetRegistrationInfo</a> function.


## -enum-fields




### -field PERF_REG_COUNTERSET_STRUCT

Gets the registration information for a counter set and all of the counters it contains as a <a href="https://msdn.microsoft.com/D220426F-7849-47DF-A411-5381FC39CA80">PERF_COUNTERSET_REG_INFO</a> block.  The block includes a <b>PERF_COUNTERSET_REG_INFO</b> structure followed by one or  

        more <a href="https://msdn.microsoft.com/34CA6EA3-DF74-4DB5-8DD0-2B0BB0162F9D">PERF_COUNTER_REG_INFO</a> structures.



### -field PERF_REG_COUNTER_STRUCT

Gets the registration information for a performance counter as  a <a href="https://msdn.microsoft.com/34CA6EA3-DF74-4DB5-8DD0-2B0BB0162F9D">PERF_COUNTER_REG_INFO</a> structure.  

        Use the <i>requestLangId</i> parameter of the <a href="https://msdn.microsoft.com/E8E83E47-2445-42AE-855F-6710FC8F789E">PerfQueryCounterSetRegistrationInfo</a> function to specify the counter identifier.  




### -field PERF_REG_COUNTERSET_NAME_STRING

Gets a null-terminated UTF16-LE string that indicates the name of the counter set.  

        Use the <i>requestLangId</i> parameter of the <a href="https://msdn.microsoft.com/E8E83E47-2445-42AE-855F-6710FC8F789E">PerfQueryCounterSetRegistrationInfo</a> function  to specify the preferred locale of the result.


### -field PERF_REG_COUNTERSET_HELP_STRING

Gets a null-terminated UTF16-LE string that contains the help string for the counter set.  

        Use the <i>requestLangId</i> parameter of the <a href="https://msdn.microsoft.com/E8E83E47-2445-42AE-855F-6710FC8F789E">PerfQueryCounterSetRegistrationInfo</a> function to specify the preferred locale of the result.


### -field PERF_REG_COUNTER_NAME_STRINGS

   Gets the names of the performance counters in the counter set as a <a href="https://msdn.microsoft.com/874A97BA-708E-4001-A7CA-1C3114577D7D">PERF_STRING_BUFFER_HEADER</a> block.  

        The block includes a <b>PERF_STRING_BUFFER_HEADER</b> structure, followed by one  

        or more <a href="https://msdn.microsoft.com/73DFA1C0-B0E8-4788-8CBA-1CFA7580F633">PERF_STRING_COUNTER_HEADER</a> structures, followed by string data that indicates the counter names.  

        Use the <i>requestLangId</i> parameter of the <a href="https://msdn.microsoft.com/E8E83E47-2445-42AE-855F-6710FC8F789E">PerfQueryCounterSetRegistrationInfo</a> function to specify the preferred locale of the result.


### -field PERF_REG_COUNTER_HELP_STRINGS

Gets the help  strings for the performance counters in the counter set as a <a href="https://msdn.microsoft.com/874A97BA-708E-4001-A7CA-1C3114577D7D">PERF_STRING_BUFFER_HEADER</a> block.  

        The block includes a <b>PERF_STRING_BUFFER_HEADER</b> structure, followed by one  

        or more <a href="https://msdn.microsoft.com/73DFA1C0-B0E8-4788-8CBA-1CFA7580F633">PERF_STRING_COUNTER_HEADER</a> structures, followed by string data that contains the help strings.  

        Use the <i>requestLangId</i> parameter of the <a href="https://msdn.microsoft.com/E8E83E47-2445-42AE-855F-6710FC8F789E">PerfQueryCounterSetRegistrationInfo</a> function to specify the preferred locale of the result.


### -field PERF_REG_PROVIDER_NAME

Gets a null-terminated UTF-16LE string that indicates the name of the provider for the counter set.


### -field PERF_REG_PROVIDER_GUID

Gets the GUID of the provider for the counter set.


### -field PERF_REG_COUNTERSET_ENGLISH_NAME

Gets a null-terminated UTF-16LE string that contains the name of the counter set in English. This value is equivalent to setting the <i>requestCode</i> parameter to <b>PERF_REG_COUNTERSET_NAME_STRING</b> and the  <i>requestLangId</i> parameter to 0 when you call the <a href="https://msdn.microsoft.com/E8E83E47-2445-42AE-855F-6710FC8F789E">PerfQueryCounterSetRegistrationInfo</a> function.



### -field PERF_REG_COUNTER_ENGLISH_NAMES

Gets the English  names of the performance counters in the counter set as a <a href="https://msdn.microsoft.com/874A97BA-708E-4001-A7CA-1C3114577D7D">PERF_STRING_BUFFER_HEADER</a> block.  

        The block includes a <b>PERF_STRING_BUFFER_HEADER</b> structure, followed by one  

        or more <a href="https://msdn.microsoft.com/73DFA1C0-B0E8-4788-8CBA-1CFA7580F633">PERF_STRING_COUNTER_HEADER</a> structures, followed by string data that indicates the counter names. This value is equivalent to setting the <i>requestCode</i> parameter to  <b>PERF_REG_COUNTER_NAME_STRINGS</b>  and the  <i>requestLangId</i> parameter to 0 when you call the <a href="https://msdn.microsoft.com/E8E83E47-2445-42AE-855F-6710FC8F789E">PerfQueryCounterSetRegistrationInfo</a> function.



## -see-also




<a href="https://msdn.microsoft.com/E8E83E47-2445-42AE-855F-6710FC8F789E">PerfQueryCounterSetRegistrationInfo</a>
 

 

