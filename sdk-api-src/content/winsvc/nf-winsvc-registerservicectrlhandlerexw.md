---
UID: NF:winsvc.RegisterServiceCtrlHandlerExW
title: RegisterServiceCtrlHandlerExW function (winsvc.h)
description: Registers a function to handle extended service control requests. (Unicode)
helpviewer_keywords: ["RegisterServiceCtrlHandlerEx", "RegisterServiceCtrlHandlerEx function", "RegisterServiceCtrlHandlerExW", "_win32_registerservicectrlhandlerex", "base.registerservicectrlhandlerex", "winsvc/RegisterServiceCtrlHandlerEx", "winsvc/RegisterServiceCtrlHandlerExW"]
old-location: base\registerservicectrlhandlerex.htm
tech.root: security
ms.assetid: 23eea346-9899-4214-88f4-9b7eb7ce1332
ms.date: 12/05/2018
ms.keywords: RegisterServiceCtrlHandlerEx, RegisterServiceCtrlHandlerEx function, RegisterServiceCtrlHandlerExA, RegisterServiceCtrlHandlerExW, _win32_registerservicectrlhandlerex, base.registerservicectrlhandlerex, winsvc/RegisterServiceCtrlHandlerEx, winsvc/RegisterServiceCtrlHandlerExA, winsvc/RegisterServiceCtrlHandlerExW
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegisterServiceCtrlHandlerExW (Unicode) and RegisterServiceCtrlHandlerExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegisterServiceCtrlHandlerExW
 - winsvc/RegisterServiceCtrlHandlerExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-service-core-l1-1-5.dll
 - api-ms-win-service-core-l1-1-4.dll
 - api-ms-win-service-core-l1-1-3.dll
 - api-ms-win-downlevel-advapi32-l2-1-0.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - sechost.dll
 - API-MS-Win-Service-Core-l1-1-0.dll
 - API-MS-Win-Service-Core-l1-1-1.dll
 - API-MS-Win-Service-Winsvc-l1-1-0.dll
 - API-MS-Win-Service-Winsvc-l1-2-0.dll
 - API-Ms-Win-Service-Core-L1-1-2.dll
api_name:
 - RegisterServiceCtrlHandlerEx
 - RegisterServiceCtrlHandlerExA
 - RegisterServiceCtrlHandlerExW
---

# RegisterServiceCtrlHandlerExW function


## -description

Registers a function to handle extended service control requests.

## -parameters

### -param lpServiceName [in]

The name of the service run by the calling thread. This is the service name that the service control program specified in the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a> function when creating the service.

### -param lpHandlerProc [in]

A pointer to the handler function to be registered. For more information, see 
<a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex">HandlerEx</a>.

### -param lpContext [in, optional]

Any user-defined data. This parameter, which is passed to the handler function, can help identify the service when multiple services share a process.

## -returns

If the function succeeds, the return value is a service status handle.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following error codes can be set by the service control manager. 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory is available to convert an ANSI string parameter to Unicode. This error does not occur for Unicode string parameters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SERVICE_NOT_IN_EXE</b></dt>
</dl>
</td>
<td width="60%">
The service entry was specified incorrectly when the process called the <a href="/windows/desktop/api/winsvc/nf-winsvc-startservicectrldispatchera">StartServiceCtrlDispatcher</a> function.

</td>
</tr>
</table>

## -remarks

The 
<a href="/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a> function of a new service should immediately call the 
<b>RegisterServiceCtrlHandlerEx</b> function to register a control handler function with the control dispatcher. This enables the control dispatcher to invoke the specified function when it receives control requests for this service. For a list of possible control codes, see <a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex">HandlerEx</a>. The threads of the calling process can use the service status handle returned by this function to identify the service in subsequent calls to the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a> function. 

The 
<b>RegisterServiceCtrlHandlerEx</b> function must be called before the first 
<a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a> call because 
<b>RegisterServiceCtrlHandlerEx</b> returns a service status handle for the caller to use so that no other service can inadvertently set this service status. In addition, the control handler must be in place to receive control requests by the time the service specifies the controls it accepts through the 
<b>SetServiceStatus</b> function.

When the control handler function is invoked with a control request, the service must call 
<a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a> to report status to the service control manager only if the service status has changed, such as when the service is processing stop or shutdown controls. If the service status has not changed, the service should not report status to the service control manager. 

The service status handle does not have to be closed.





> [!NOTE]
> The winsvc.h header defines RegisterServiceCtrlHandlerEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a>



<a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex">HandlerEx</a>



<a href="/windows/desktop/Services/service-control-handler-function">Service Control Handler Function</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>



<a href="/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a>
