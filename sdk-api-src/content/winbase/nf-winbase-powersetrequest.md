---
UID: NF:winbase.PowerSetRequest
title: PowerSetRequest function (winbase.h)
description: Increments the count of power requests of the specified type for a power request object.
helpviewer_keywords: ["PowerRequestAwayModeRequired","PowerRequestDisplayRequired","PowerRequestExecutionRequired","PowerRequestSystemRequired","PowerSetRequest","PowerSetRequest function","base.powersetrequest","winbase/PowerSetRequest"]
old-location: base\powersetrequest.htm
tech.root: base
ms.assetid: 85249de8-5832-4f25-bbd9-3576cfd1caa0
ms.date: 12/05/2018
ms.keywords: PowerRequestAwayModeRequired, PowerRequestDisplayRequired, PowerRequestExecutionRequired, PowerRequestSystemRequired, PowerSetRequest, PowerSetRequest function, base.powersetrequest, winbase/PowerSetRequest
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PowerSetRequest
 - winbase/PowerSetRequest
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - PowerSetRequest
---

# PowerSetRequest function


## -description

Increments the count of power requests of the specified type for a power request object.

## -parameters

### -param PowerRequest [in]

A handle to a power request object.

### -param RequestType [in]

The power request type to be incremented. This parameter can be one of the following values.

| Value  | Description |
|--------|-------------|
| PowerRequestDisplayRequired | The display remains on even if there is no user input for an extended period of time.<br/><br/><div class="alert"><b>Note: </b>A <b>PowerRequestSystemRequired</b> must be taken in addition to a <b>PowerRequestDisplayRequired</b> to ensure the display stays on and the system does not enter sleep for the duration of the request.</div> |
| PowerRequestSystemRequired | The system continues to run instead of entering sleep after a period of user inactivity. |
| PowerRequestAwayModeRequired | The system enters away mode instead of sleep in response to explicit action by the user. In away mode, the system continues to run but turns off audio and video to give the appearance of sleep. <b>PowerRequestAwayModeRequired</b> is only applicable on Traditional Sleep (S3) systems. |
| PowerRequestExecutionRequired | The calling process continues to run instead of being suspended or terminated by process lifetime management mechanisms. When and how long the process is allowed to run depends on the operating system and  power policy settings.<br/><br/>On Traditional Sleep (S3) systems, an active <b>PowerRequestExecutionRequired</b> request implies <b>PowerRequestSystemRequired</b>. |

## -returns

If the function succeeds, it returns a nonzero value.

If the function fails, it returns zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

On Modern Standby systems on DC power, system and execution required power requests are terminated 5 minutes after the system sleep timeout has expired.

Except for <b>PowerRequestAwayModeRequired</b> on Traditional Sleep (S3) systems, power requests are terminated upon user-initiated system sleep entry (power button, lid close or selecting **Sleep** from the **Start** menu).

To conserve power and provide the best user experience, applications that use power requests should follow these best practices:

* When creating a power request, provide a localized text string that describes the reason for the request in the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-reason_context">REASON_CONTEXT</a> structure.
* Call <b>PowerSetRequest</b> immediately before the scenario that requires the request.
* Call <a href="/windows/desktop/api/winbase/nf-winbase-powerclearrequest">PowerClearRequest</a> to decrement the reference count for the request as soon as the scenario is finished.
* Clean up all request objects and associated handles before the process exits or the service stops.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-powerclearrequest">PowerClearRequest</a>

<a href="/windows/desktop/api/winbase/nf-winbase-powercreaterequest">PowerCreateRequest</a>
