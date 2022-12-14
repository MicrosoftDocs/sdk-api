---
UID: NF:roerrorapi.RoReportUnhandledError
title: RoReportUnhandledError function
description: Triggers the Global Error Handler when an unhandled exception occurs.
helpviewer_keywords: ["RoReportUnhandledError","RoReportUnhandledError function [Windows Runtime]","roerrorapi/RoReportUnhandledError","winrt.roreportunhandlederror"]
old-location: winrt\roreportunhandlederror.htm
tech.root: WinRT
ms.assetid: DE8F29B4-505C-480E-9258-9E5300BEA3F0
ms.date: 12/5/2018
ms.keywords: RoReportUnhandledError, RoReportUnhandledError function [Windows Runtime], roerrorapi/RoReportUnhandledError, winrt.roreportunhandlederror
req.header: roerrorapi.h
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
req.lib: Runtimeobject.lib
req.dll: Api-ms-win-core-winrt-error-l1-1-1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - RoReportUnhandledError
 - roerrorapi/RoReportUnhandledError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-winrt-error-l1-1-1.dll
 - ComBase.dll
api_name:
 - RoReportUnhandledError
---

# RoReportUnhandledError function


## -description

Triggers the Global Error Handler when an unhandled exception occurs.

## -parameters

### -param pRestrictedErrorInfo [in]

The error to report. Call the <a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-getrestrictederrorinfo">GetRestrictedErrorInfo</a> function to get the <a href="/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-irestrictederrorinfo">IRestrictedErrorInfo</a> that represents the error.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>RoReportUnhandledError</b> function enables language projections to trigger execution of the Global Error Handler when an exception reaches the top of the stack, which normally would terminate the application.

## -see-also

<a href="/windows/desktop/api/roerrorapi/nf-roerrorapi-getrestrictederrorinfo">GetRestrictedErrorInfo</a>



<a href="https://msdn.microsoft.com/295bcf8f-c264-48d9-a460-c2a0a2fb1201">ICoreApplicationUnhandledError</a>