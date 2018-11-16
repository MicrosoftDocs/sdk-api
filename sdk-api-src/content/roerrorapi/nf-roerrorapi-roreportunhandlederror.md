---
UID: NF:roerrorapi.RoReportUnhandledError
title: RoReportUnhandledError function
author: windows-sdk-content
description: Triggers the Global Error Handler when an unhandled exception occurs.
old-location: winrt\roreportunhandlederror.htm
tech.root: WinRT
ms.assetid: DE8F29B4-505C-480E-9258-9E5300BEA3F0
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: RoReportUnhandledError, RoReportUnhandledError function [Windows Runtime], roerrorapi/RoReportUnhandledError, winrt.roreportunhandlederror
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- RoReportUnhandledError
: 
---

# RoReportUnhandledError function


## -description


Triggers the Global Error Handler when an unhandled exception occurs.


## -parameters




### -param pRestrictedErrorInfo [in]

The error to report. Call the <a href="https://msdn.microsoft.com/CA459E57-90D5-44F6-A896-4E1C2FA0DC57">GetRestrictedErrorInfo</a> function to get the <a href="https://msdn.microsoft.com/1af8d4bf-1217-44ca-b0dd-9a6feda16100">IRestrictedErrorInfo</a> that represents the error.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>RoReportUnhandledError</b> function enables language projections to trigger execution of the Global Error Handler when an exception reaches the top of the stack, which normally would terminate the application.




## -see-also




<a href="https://msdn.microsoft.com/CA459E57-90D5-44F6-A896-4E1C2FA0DC57">GetRestrictedErrorInfo</a>



<a href="https://msdn.microsoft.com/295bcf8f-c264-48d9-a460-c2a0a2fb1201">ICoreApplicationUnhandledError</a>
 

 

