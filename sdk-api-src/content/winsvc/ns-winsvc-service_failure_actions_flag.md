---
UID: NS:winsvc._SERVICE_FAILURE_ACTIONS_FLAG
title: SERVICE_FAILURE_ACTIONS_FLAG (winsvc.h)
description: Contains the failure actions flag setting of a service. This setting determines when failure actions are to be executed.
helpviewer_keywords: ["*LPSERVICE_FAILURE_ACTIONS_FLAG","LPSERVICE_FAILURE_ACTIONS_FLAG","LPSERVICE_FAILURE_ACTIONS_FLAG structure pointer","SERVICE_FAILURE_ACTIONS_FLAG","SERVICE_FAILURE_ACTIONS_FLAG structure","base.service_failure_actions_flag","winsvc/LPSERVICE_FAILURE_ACTIONS_FLAG","winsvc/SERVICE_FAILURE_ACTIONS_FLAG"]
old-location: base\service_failure_actions_flag.htm
tech.root: security
ms.assetid: 49736b26-9565-4d56-abcd-1585b692ff12
ms.date: 12/05/2018
ms.keywords: '*LPSERVICE_FAILURE_ACTIONS_FLAG, LPSERVICE_FAILURE_ACTIONS_FLAG, LPSERVICE_FAILURE_ACTIONS_FLAG structure pointer, SERVICE_FAILURE_ACTIONS_FLAG, SERVICE_FAILURE_ACTIONS_FLAG structure, base.service_failure_actions_flag, winsvc/LPSERVICE_FAILURE_ACTIONS_FLAG, winsvc/SERVICE_FAILURE_ACTIONS_FLAG'
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SERVICE_FAILURE_ACTIONS_FLAG, *LPSERVICE_FAILURE_ACTIONS_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVICE_FAILURE_ACTIONS_FLAG
 - winsvc/_SERVICE_FAILURE_ACTIONS_FLAG
 - LPSERVICE_FAILURE_ACTIONS_FLAG
 - winsvc/LPSERVICE_FAILURE_ACTIONS_FLAG
 - SERVICE_FAILURE_ACTIONS_FLAG
 - winsvc/SERVICE_FAILURE_ACTIONS_FLAG
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
 - SERVICE_FAILURE_ACTIONS_FLAG
---

# SERVICE_FAILURE_ACTIONS_FLAG structure


## -description

Contains the failure actions flag setting of a service. This setting determines when failure actions are to be executed.

## -struct-fields

### -field fFailureActionsOnNonCrashFailures

If this member is <b>TRUE</b> and the service has configured failure actions, the failure actions are queued if the service process terminates without reporting a status of SERVICE_STOPPED or if it enters the SERVICE_STOPPED state but the <b>dwWin32ExitCode</b> member of the <a href="/windows/desktop/api/winsvc/ns-winsvc-service_status">SERVICE_STATUS</a> structure is not ERROR_SUCCESS (0).

If this member is <b>FALSE</b> and the service has configured failure actions, the failure actions are queued only if the service terminates without reporting a status of SERVICE_STOPPED.

This setting is ignored unless the service has configured failure actions. For information on configuring failure actions, see <a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a">ChangeServiceConfig2</a>.

## -remarks

The change takes effect the next time the system is started.

It can be useful to set this flag if your service has common failure paths where is it possible that the service could recover.

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a">ChangeServiceConfig2</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfig2a">QueryServiceConfig2</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_failure_actionsa">SERVICE_FAILURE_ACTIONS</a>