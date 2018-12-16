---
UID: NF:rtlsupportapi.RtlRaiseException
title: RtlRaiseException function
author: windows-sdk-content
description: Raises an exception.
old-location: winprog\rtlraiseexception.htm
tech.root: devnotes
ms.assetid: 0d43418a-1c80-4f5e-a0fe-5bc3adac847c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RtlRaiseException, RtlRaiseException function [Windows API], rtlsupportapi/RtlRaiseException, winprog.rtlraiseexception
ms.topic: function
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
req.lib: 
req.dll: Ntdll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ntdll.dll
 - API-MS-Win-Core-RTLSupport-l1-1-0.dll
 - API-MS-Win-Core-RTLSupport-l1-2-0.dll
api_name:
 - RtlRaiseException
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtlRaiseException function


## -description


Raises an exception.


## -parameters




### -param ExceptionRecord [in]

Address of an <a href="https://msdn.microsoft.com/85a64178-bdcb-4293-9363-289c654730a2">EXCEPTION_RECORD</a> structure 
      that describes the exception, and the parameters of the exception, that is raised. Raising a software exception 
      captures the machine state of the current thread in a context record. The 
      <b>ExceptionAddress</b> member of the exception record is set to the caller's return 
      address.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/85a64178-bdcb-4293-9363-289c654730a2">EXCEPTION_RECORD</a>
 

 

