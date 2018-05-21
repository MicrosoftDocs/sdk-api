---
UID: NF:roerrorapi.RoCaptureErrorContext
title: RoCaptureErrorContext function
author: windows-driver-content
description: Saves the current error context so that it's available for later calls to the RoFailFastWithErrorContext function.
old-location: winrt\rocaptureerrorcontext.htm
old-project: WinRT
ms.assetid: 4102CAD6-B5EC-4633-91CC-D56F6C0E287E
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: RoCaptureErrorContext, RoCaptureErrorContext function [Windows Runtime], roerrorapi/RoCaptureErrorContext, winrt.rocaptureerrorcontext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: roerrorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	ComBase.dll
-	API-MS-Win-Core-WinRT-error-l1-1-0.dll
-	API-MS-Win-Core-WinRT-error-l1-1-1.dll
api_name:
-	RoCaptureErrorContext
product: Windows
targetos: Windows
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RoCaptureErrorContext function


## -description


Saves the current error context so that it's available for later calls to the <a href="https://msdn.microsoft.com/1BD47795-1B5E-42A4-B88F-7DE5160668E7">RoFailFastWithErrorContext</a> function.


## -parameters




### -param hr

TBD




#### - hrError

The <b>HRESULT</b> associated with the error.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>RoCaptureErrorContext</b> function captures the context associated with an error, including the stack-backtrace. This information is stored in the restricted error object and is available to the Windows Error Reporting (WER) service, if WER is  enabled, and if a subsequent call is made to the <a href="https://msdn.microsoft.com/1BD47795-1B5E-42A4-B88F-7DE5160668E7">RoFailFastWithErrorContext</a> function from the same thread.

To use <b>RoCaptureErrorContext</b> function with <a href="https://msdn.microsoft.com/ED647880-5A18-4F75-B7E5-3B9BF36229D3">RoOriginateError</a>, call <b>RoOriginateError</b> first, and then call <b>RoCaptureErrorContext</b>.  Calling in the reverse order may cause the error context to be lost.




## -see-also




<a href="https://msdn.microsoft.com/1af8d4bf-1217-44ca-b0dd-9a6feda16100">IRestrictedErrorInfo</a>



<a href="https://msdn.microsoft.com/1BD47795-1B5E-42A4-B88F-7DE5160668E7">RoFailFastWithErrorContext</a>



<a href="https://msdn.microsoft.com/ED647880-5A18-4F75-B7E5-3B9BF36229D3">RoOriginateError</a>



<a href="https://msdn.microsoft.com/FC75DDA5-59BA-4CCF-93CC-8D0BB2AB415B">RoOriginateErrorW</a>
 

 

