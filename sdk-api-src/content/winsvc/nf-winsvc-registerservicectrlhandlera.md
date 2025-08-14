---
UID: NF:winsvc.RegisterServiceCtrlHandlerA
title: RegisterServiceCtrlHandlerA function (winsvc.h)
description: Registers a function to handle service control requests. (ANSI)
helpviewer_keywords: ["RegisterServiceCtrlHandlerA", "winsvc/RegisterServiceCtrlHandlerA"]
old-location: base\registerservicectrlhandler.htm
tech.root: security
ms.assetid: 31ec28fe-8774-48fc-91ba-6fa43108e2cc
ms.date: 12/05/2018
ms.keywords: RegisterServiceCtrlHandler, RegisterServiceCtrlHandler function, RegisterServiceCtrlHandlerA, RegisterServiceCtrlHandlerW, _win32_registerservicectrlhandler, base.registerservicectrlhandler, winsvc/RegisterServiceCtrlHandler, winsvc/RegisterServiceCtrlHandlerA, winsvc/RegisterServiceCtrlHandlerW
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RegisterServiceCtrlHandlerW (Unicode) and RegisterServiceCtrlHandlerA (ANSI)
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
 - RegisterServiceCtrlHandlerA
 - winsvc/RegisterServiceCtrlHandlerA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-advapi32-l2-1-0.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - sechost.dll
 - API-MS-Win-Service-Winsvc-l1-1-0.dll
 - API-MS-Win-Service-Winsvc-l1-2-0.dll
api_name:
 - RegisterServiceCtrlHandler
 - RegisterServiceCtrlHandlerA
 - RegisterServiceCtrlHandlerW
---

# RegisterServiceCtrlHandlerA function


## -description

Registers a function to handle  service control requests.

This function has been superseded by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa">RegisterServiceCtrlHandlerEx</a> function. A service can use either function, but the new function supports user-defined context data, and the new handler function supports additional extended control codes.

## -parameters

### -param lpServiceName [in]

The name of the service run by the calling thread. This is the service name that the service control program specified in the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a> function when creating the service. 




If the service type is SERVICE_WIN32_OWN_PROCESS, the function does not verify that the specified name is valid, because there is only one registered service in the process.

### -param lpHandlerProc [in]

A pointer to the handler function to be registered. For more information, see 
<a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function">Handler</a>.

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
<b>RegisterServiceCtrlHandler</b> function to register a control handler function with the control dispatcher. This enables the control dispatcher to invoke the specified function when it receives control requests for this service. For a list of possible control codes, see <a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function">Handler</a>. The threads of the calling process can use the service status handle returned by this function to identify the service in subsequent calls to the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a> function.

The 
<b>RegisterServiceCtrlHandler</b> function must be called before the first 
<a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a> call because 
<b>RegisterServiceCtrlHandler</b> returns a service status handle for the caller to use so that no other service can inadvertently set this service status. In addition, the control handler must be in place to receive control requests by the time the service specifies the controls it accepts through the 
<b>SetServiceStatus</b> function.

When the control handler function is invoked with a control request, the service must call 
<a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a> to report status to the service control manager only if the service status has changed, such as when the service is processing stop or shutdown controls. If the service status has not changed, the service should not report status to the service control manager. 

The service status handle does not have to be closed.


#### Examples

For an example, see 
<a href="/windows/desktop/Services/writing-a-servicemain-function">Writing a ServiceMain Function</a>.

<div class="code"></div>




> [!NOTE]
> The winsvc.h header defines RegisterServiceCtrlHandler as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-createservicea">CreateService</a>



<a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function">Handler</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-registerservicectrlhandlerexa">RegisterServiceCtrlHandlerEx</a>



<a href="/windows/desktop/Services/service-control-handler-function">Service Control Handler Function</a>



<a href="/windows/desktop/Services/service-functions">Service Functions</a>



<a href="/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-setservicestatus">SetServiceStatus</a>
