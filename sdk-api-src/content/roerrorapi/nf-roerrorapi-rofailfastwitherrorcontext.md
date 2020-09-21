---
UID: NF:roerrorapi.RoFailFastWithErrorContext
title: RoFailFastWithErrorContext function
description: Raises a non-continuable exception in the current process.
helpviewer_keywords: ["RoFailFastWithErrorContext","RoFailFastWithErrorContext function [Windows Runtime]","roerrorapi/RoFailFastWithErrorContext","winrt.rofailfastwitherrorcontext"]
old-location: winrt\rofailfastwitherrorcontext.htm
tech.root: WinRT
ms.assetid: 1BD47795-1B5E-42A4-B88F-7DE5160668E7
ms.date: 12/5/2018
ms.keywords: RoFailFastWithErrorContext, RoFailFastWithErrorContext function [Windows Runtime], roerrorapi/RoFailFastWithErrorContext, winrt.rofailfastwitherrorcontext
req.header: roerrorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: RuntimeObject.lib
req.dll: ComBase.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - RoFailFastWithErrorContext
 - roerrorapi/RoFailFastWithErrorContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ComBase.dll
 - API-MS-Win-Core-WinRT-error-l1-1-0.dll
 - API-MS-Win-Core-WinRT-error-l1-1-1.dll
api_name:
 - RoFailFastWithErrorContext
---

# RoFailFastWithErrorContext function


## -description

Raises a non-continuable exception in the current process.

## -parameters

### -param hrError [in]

The <b>HRESULT</b> associated with the current error. The exception is raised for any value of <i>hrError</i>.

## -remarks

The <b>RoFailFastWithErrorContext</b> function raises a non-continuable exception in the current process when an unhandled failure is encountered, which  prevents the process from continuing execution in an undefined state.

Call the <b>RoFailFastWithErrorContext</b> function when a failure occurs in a completion delegate for a completed asynchronous operation, or  when a failure occurs in an event handler when an event is raised.

The process that calls <b>RoFailFastWithErrorContext</b> is terminated by a call to <a href="/previous-versions/dd408166(v=vs.85)">RaiseFailFastException</a>.  The function does not validate the parameters and raises an exception for any value of the inputs.

Call the <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rocaptureerrorcontext">RoCaptureErrorContext</a> function to save an <a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a> object that's associated with the current thread. The <b>RoFailFastWithErrorContext</b> function uses this contextual information to report the error call stack to the Windows Error Reporting service (WER), if it's enabled.

## -see-also

<a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a>



<a href="/previous-versions/dd408166(v=vs.85)">RaiseFailFastException</a>



<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-rocaptureerrorcontext">RoCaptureErrorContext</a>