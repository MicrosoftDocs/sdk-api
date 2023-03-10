---
UID: NS:winnt._EXCEPTION_POINTERS
title: EXCEPTION_POINTERS (winnt.h)
description: Contains an exception record with a machine-independent description of an exception and a context record with a machine-dependent description of the processor context at the time of the exception.
helpviewer_keywords: ["*PEXCEPTION_POINTERS","EXCEPTION_POINTERS","EXCEPTION_POINTERS structure","PEXCEPTION_POINTERS","PEXCEPTION_POINTERS structure pointer","_EXCEPTION_POINTERS","_win32_exception_pointers_str","base.exception_pointers_str","winnt/EXCEPTION_POINTERS","winnt/PEXCEPTION_POINTERS"]
old-location: base\exception_pointers_str.htm
tech.root: Debug
ms.assetid: 57e8cb3a-1b11-45b9-9676-3b6dc600d225
ms.date: 12/05/2018
ms.keywords: '*PEXCEPTION_POINTERS, EXCEPTION_POINTERS, EXCEPTION_POINTERS structure, PEXCEPTION_POINTERS, PEXCEPTION_POINTERS structure pointer, _EXCEPTION_POINTERS, _win32_exception_pointers_str, base.exception_pointers_str, winnt/EXCEPTION_POINTERS, winnt/PEXCEPTION_POINTERS'
req.header: winnt.h
req.include-header: Windows.h
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
req.typenames: EXCEPTION_POINTERS, *PEXCEPTION_POINTERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EXCEPTION_POINTERS
 - winnt/_EXCEPTION_POINTERS
 - PEXCEPTION_POINTERS
 - winnt/PEXCEPTION_POINTERS
 - EXCEPTION_POINTERS
 - winnt/EXCEPTION_POINTERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - EXCEPTION_POINTERS
---

# EXCEPTION_POINTERS structure


## -description

Contains an exception record with a machine-independent description of an exception and a context record with a machine-dependent description of the processor context at the time of the exception.

## -struct-fields

### -field ExceptionRecord

A pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-exception_record">EXCEPTION_RECORD</a> structure that contains a machine-independent description of the exception.

### -field ContextRecord

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-context">CONTEXT</a> structure that contains a processor-specific description of the state of the processor at the time of the exception.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a>



<a href="/windows/desktop/api/winnt/ns-winnt-exception_record">EXCEPTION_RECORD</a>



<a href="/windows/desktop/Debug/getexceptioninformation">GetExceptionInformation</a>
