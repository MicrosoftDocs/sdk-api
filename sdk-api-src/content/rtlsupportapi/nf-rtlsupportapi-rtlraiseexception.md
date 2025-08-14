---
UID: NF:rtlsupportapi.RtlRaiseException
title: RtlRaiseException function (rtlsupportapi.h)
description: Raises an exception.
helpviewer_keywords: ["RtlRaiseException","RtlRaiseException function [Windows API]","rtlsupportapi/RtlRaiseException","winprog.rtlraiseexception"]
old-location: winprog\rtlraiseexception.htm
tech.root: winprog
ms.assetid: 0d43418a-1c80-4f5e-a0fe-5bc3adac847c
ms.date: 12/05/2018
ms.keywords: RtlRaiseException, RtlRaiseException function [Windows API], rtlsupportapi/RtlRaiseException, winprog.rtlraiseexception
req.header: rtlsupportapi.h
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
req.lib: ntdll.lib
req.dll: ntdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtlRaiseException
 - rtlsupportapi/RtlRaiseException
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-rtlsupport-l1-2-2.dll
 - api-ms-win-core-rtlsupport-l1-2-1.dll
 - ntdll.dll
 - API-MS-Win-Core-RTLSupport-l1-1-0.dll
 - API-MS-Win-Core-RTLSupport-l1-2-0.dll
api_name:
 - RtlRaiseException
---

# RtlRaiseException function


## -description

Raises an exception.

## -parameters

### -param ExceptionRecord [in]

Address of an <a href="/windows/desktop/api/winnt/ns-winnt-exception_record">EXCEPTION_RECORD</a> structure 
      that describes the exception, and the parameters of the exception, that is raised. Raising a software exception 
      captures the machine state of the current thread in a context record. The 
      <b>ExceptionAddress</b> member of the exception record is set to the caller's return 
      address.

## -returns

This function does not return a value.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-exception_record">EXCEPTION_RECORD</a>