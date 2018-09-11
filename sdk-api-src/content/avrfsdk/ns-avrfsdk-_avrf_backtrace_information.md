---
UID: NS:avrfsdk._AVRF_BACKTRACE_INFORMATION
title: "_AVRF_BACKTRACE_INFORMATION"
author: windows-sdk-content
description: Contains information about backtraces performed.
old-location: winprog\avrf_backtrace_information.htm
tech.root: DevNotes
ms.assetid: 634d9569-469c-4dc7-9192-217af0937b6c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PAVRF_BACKTRACE_INFORMATION, AVRF_BACKTRACE_INFORMATION, AVRF_BACKTRACE_INFORMATION structure [Windows API], _AVRF_BACKTRACE_INFORMATION, avrfsdk/AVRF_BACKTRACE_INFORMATION, base.avrf_backtrace_information, winprog.avrf_backtrace_information"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Avrfsdk.h
api_name:
 - AVRF_BACKTRACE_INFORMATION
product: Windows
targetos: Windows
req.typenames: AVRF_BACKTRACE_INFORMATION, *PAVRF_BACKTRACE_INFORMATION
req.redist: 
---

# _AVRF_BACKTRACE_INFORMATION structure


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




<a href="https://msdn.microsoft.com/99cb9005-9cfc-44fb-b09f-fed0541cda37">Resource Enumeration</a>



<a href="https://msdn.microsoft.com/e1715f2a-5928-44e6-afbf-f2f0ab0ba3dd">VerifierEnumerateResource</a>
 

 

