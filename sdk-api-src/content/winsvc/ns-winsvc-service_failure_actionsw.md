---
UID: NS:winsvc._SERVICE_FAILURE_ACTIONSW
title: SERVICE_FAILURE_ACTIONSW (winsvc.h)
description: Represents the action the service controller should take on each failure of a service. A service is considered failed when it terminates without reporting a status of SERVICE_STOPPED to the service controller. (Unicode)
helpviewer_keywords: ["*LPSERVICE_FAILURE_ACTIONSW","LPSERVICE_FAILURE_ACTIONS","LPSERVICE_FAILURE_ACTIONS structure pointer","SERVICE_FAILURE_ACTIONS","SERVICE_FAILURE_ACTIONS structure","SERVICE_FAILURE_ACTIONSA","SERVICE_FAILURE_ACTIONSW","_win32_service_failure_actions_str","base.service_failure_actions_str","winsvc/LPSERVICE_FAILURE_ACTIONS","winsvc/SERVICE_FAILURE_ACTIONS","winsvc/SERVICE_FAILURE_ACTIONSA","winsvc/SERVICE_FAILURE_ACTIONSW"]
old-location: base\service_failure_actions_str.htm
tech.root: security
ms.assetid: 180ca6d9-f2c3-4ea1-b2c6-319d08ef88ee
ms.date: 12/05/2018
ms.keywords: '*LPSERVICE_FAILURE_ACTIONSW, LPSERVICE_FAILURE_ACTIONS, LPSERVICE_FAILURE_ACTIONS structure pointer, SERVICE_FAILURE_ACTIONS, SERVICE_FAILURE_ACTIONS structure, SERVICE_FAILURE_ACTIONSA, SERVICE_FAILURE_ACTIONSW, _win32_service_failure_actions_str, base.service_failure_actions_str, winsvc/LPSERVICE_FAILURE_ACTIONS, winsvc/SERVICE_FAILURE_ACTIONS, winsvc/SERVICE_FAILURE_ACTIONSA, winsvc/SERVICE_FAILURE_ACTIONSW'
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SERVICE_FAILURE_ACTIONSW (Unicode) and SERVICE_FAILURE_ACTIONSA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SERVICE_FAILURE_ACTIONSW, *LPSERVICE_FAILURE_ACTIONSW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVICE_FAILURE_ACTIONSW
 - winsvc/_SERVICE_FAILURE_ACTIONSW
 - LPSERVICE_FAILURE_ACTIONSW
 - winsvc/LPSERVICE_FAILURE_ACTIONSW
 - SERVICE_FAILURE_ACTIONSW
 - winsvc/SERVICE_FAILURE_ACTIONSW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsvc.h
api_name:
 - SERVICE_FAILURE_ACTIONS
 - SERVICE_FAILURE_ACTIONSA
 - SERVICE_FAILURE_ACTIONSW
---

# SERVICE_FAILURE_ACTIONSW structure


## -description

Represents the action the service controller should take on each failure of a service. A service is considered failed when it terminates without reporting a status of <b>SERVICE_STOPPED</b> to the service controller.

To configure additional circumstances under which the failure actions are to be executed, see <a href="/windows/desktop/api/winsvc/ns-winsvc-service_failure_actions_flag">SERVICE_FAILURE_ACTIONS_FLAG</a>.

## -struct-fields

### -field dwResetPeriod

The time after which to reset the failure count to zero if there are no failures, in seconds. Specify <b>INFINITE</b> to indicate that this value should never be reset.

### -field lpRebootMsg

The message to be broadcast to server users before rebooting in response to the <b>SC_ACTION_REBOOT</b> service controller action. 




If this value is <b>NULL</b>, the reboot message is unchanged. If the value is an empty string (""), the reboot message is deleted and no message is broadcast.

This member can specify a localized string using the following format:

@[<i>path</i>\]<i>dllname</i>,-<i>strID</i>

The string with identifier <i>strID</i> is loaded from <i>dllname</i>; the <i>path</i> is optional. For more information, see <a href="/windows/desktop/api/winreg/nf-winreg-regloadmuistringa">RegLoadMUIString</a>.

<b>Windows Server 2003 and Windows XP:  </b>Localized strings are not supported until Windows Vista.

### -field lpCommand

The command line of the process for the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> function to execute in response to the <b>SC_ACTION_RUN_COMMAND</b> service controller action. This process runs under the same account as the service. 




If this value is <b>NULL</b>, the command is unchanged. If the value is an empty string (""), the command is deleted and no program is run when the service fails.

### -field cActions

The number of elements in the <b>lpsaActions</b> array. 




If this value is 0, but <b>lpsaActions</b> is not NULL, the reset period and array of failure actions are deleted.

### -field cActions.range

### -field cActions.range.0

### -field cActions.range.1024

### -field lpsaActions

A pointer to an array of 
<a href="/windows/desktop/api/winsvc/ns-winsvc-sc_action">SC_ACTION</a> structures. 




If this value is NULL, the <b>cActions</b> and <b>dwResetPeriod</b> members are ignored.

### -field lpsaActions.size_is

### -field lpsaActions.size_is.cActions

## -remarks

The service control manager counts the number of times each service has failed since the system booted. The count is reset to 0 if the service has not failed for <b>dwResetPeriod</b> seconds. When the service fails for the <i>N</i>th time, the service controller performs the action specified in element [<i>N</i>-1] of the <b>lpsaActions</b> array. If <i>N</i> is greater than <i>cActions</i>, the service controller repeats the last action in the array.





> [!NOTE]
> The winsvc.h header defines SERVICE_FAILURE_ACTIONS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a">ChangeServiceConfig2</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfig2a">QueryServiceConfig2</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-sc_action">SC_ACTION</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_failure_actions_flag">SERVICE_FAILURE_ACTIONS_FLAG</a>
