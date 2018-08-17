---
UID: NS:winsvc._SERVICE_FAILURE_ACTIONS_FLAG
title: "_SERVICE_FAILURE_ACTIONS_FLAG"
author: windows-sdk-content
description: Contains the failure actions flag setting of a service. This setting determines when failure actions are to be executed.
old-location: base\service_failure_actions_flag.htm
old-project: services
ms.assetid: 49736b26-9565-4d56-abcd-1585b692ff12
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: "*LPSERVICE_FAILURE_ACTIONS_FLAG, LPSERVICE_FAILURE_ACTIONS_FLAG, LPSERVICE_FAILURE_ACTIONS_FLAG structure pointer, SERVICE_FAILURE_ACTIONS_FLAG, SERVICE_FAILURE_ACTIONS_FLAG structure, _SERVICE_FAILURE_ACTIONS_FLAG, base.service_failure_actions_flag, winsvc/LPSERVICE_FAILURE_ACTIONS_FLAG, winsvc/SERVICE_FAILURE_ACTIONS_FLAG"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winsvc.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: SERVICE_FAILURE_ACTIONS_FLAG, *LPSERVICE_FAILURE_ACTIONS_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsvc.h
api_name:
 - SERVICE_FAILURE_ACTIONS_FLAG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _SERVICE_FAILURE_ACTIONS_FLAG structure


## -description


Contains the failure actions flag setting of a service. This setting determines when failure actions are to be executed.


## -struct-fields




### -field fFailureActionsOnNonCrashFailures

If this member is <b>TRUE</b> and the service has configured failure actions, the failure actions are queued if the service process terminates without reporting a status of SERVICE_STOPPED or if it enters the SERVICE_STOPPED state but the <b>dwWin32ExitCode</b> member of the <a href="https://msdn.microsoft.com/d268609b-d442-4d0f-9d49-ed23fee84961">SERVICE_STATUS</a> structure is not ERROR_SUCCESS (0).

If this member is <b>FALSE</b> and the service has configured failure actions, the failure actions are queued only if the service terminates without reporting a status of SERVICE_STOPPED.

This setting is ignored unless the service has configured failure actions. For information on configuring failure actions, see <a href="https://msdn.microsoft.com/6e5b79ed-52e1-460e-b076-01afbd08775c">ChangeServiceConfig2</a>.


## -remarks



The change takes effect the next time the system is started.

It can be useful to set this flag if your service has common failure paths where is it possible that the service could recover.




## -see-also




<a href="https://msdn.microsoft.com/6e5b79ed-52e1-460e-b076-01afbd08775c">ChangeServiceConfig2</a>



<a href="https://msdn.microsoft.com/cb090e59-aeff-4420-bb7c-912a4911006f">QueryServiceConfig2</a>



<a href="https://msdn.microsoft.com/180ca6d9-f2c3-4ea1-b2c6-319d08ef88ee">SERVICE_FAILURE_ACTIONS</a>
 

 

