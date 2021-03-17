---
UID: NS:winsvc._SERVICE_DELAYED_AUTO_START_INFO
title: SERVICE_DELAYED_AUTO_START_INFO (winsvc.h)
description: Contains the delayed auto-start setting of an auto-start service.
helpviewer_keywords: ["*LPSERVICE_DELAYED_AUTO_START_INFO","LPSERVICE_DELAYED_AUTO_START_INFO","LPSERVICE_DELAYED_AUTO_START_INFO structure pointer","SERVICE_DELAYED_AUTO_START_INFO","SERVICE_DELAYED_AUTO_START_INFO structure","base.service_delayed_auto_start_info","winsvc/LPSERVICE_DELAYED_AUTO_START_INFO","winsvc/SERVICE_DELAYED_AUTO_START_INFO"]
old-location: base\service_delayed_auto_start_info.htm
tech.root: security
ms.assetid: 16117450-eb73-47de-8be7-c7aff3d44c81
ms.date: 12/05/2018
ms.keywords: '*LPSERVICE_DELAYED_AUTO_START_INFO, LPSERVICE_DELAYED_AUTO_START_INFO, LPSERVICE_DELAYED_AUTO_START_INFO structure pointer, SERVICE_DELAYED_AUTO_START_INFO, SERVICE_DELAYED_AUTO_START_INFO structure, base.service_delayed_auto_start_info, winsvc/LPSERVICE_DELAYED_AUTO_START_INFO, winsvc/SERVICE_DELAYED_AUTO_START_INFO'
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
req.typenames: SERVICE_DELAYED_AUTO_START_INFO, *LPSERVICE_DELAYED_AUTO_START_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVICE_DELAYED_AUTO_START_INFO
 - winsvc/_SERVICE_DELAYED_AUTO_START_INFO
 - LPSERVICE_DELAYED_AUTO_START_INFO
 - winsvc/LPSERVICE_DELAYED_AUTO_START_INFO
 - SERVICE_DELAYED_AUTO_START_INFO
 - winsvc/SERVICE_DELAYED_AUTO_START_INFO
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
 - SERVICE_DELAYED_AUTO_START_INFO
---

# SERVICE_DELAYED_AUTO_START_INFO structure


## -description

Contains the delayed auto-start setting of an auto-start service.

## -struct-fields

### -field fDelayedAutostart

If this member is <b>TRUE</b>, the service is started after other auto-start services are started plus a short delay. Otherwise, the service is started during system boot.

This setting is ignored unless the service is an auto-start service.

## -remarks

Any service can be marked as a delayed auto-start service; however, this setting has no effect unless the service is an auto-start service. The change takes effect the next time the system is started.

The service control manager (SCM) supports delayed auto-start services to improve system performance at boot time without affecting the user experience. The SCM makes a list of delayed auto-start services during boot and starts them one at a time after the delay has passed, honoring dependencies. There is no specific time guarantee as to when the service will be started. To minimize the impact on the user, the <a href="/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a> thread for the service is started with THREAD_PRIORITY_LOWEST. Threads that are started by the <i>ServiceMain</i> thread should also be run at a low priority. After the service has reported that it has entered the SERVICE_RUNNING state, the priority of the <i>ServiceMain</i> thread is raised to THREAD_PRIORITY_NORMAL.

A delayed auto-start service cannot be a member of a load ordering group. It can depend on another auto-start service. An auto-start service can depend on a delayed auto-start service, but this is not generally desirable as the SCM must start the dependent delayed auto-start service at boot.

If a delayed auto-start service is demand-started using the <a href="/windows/desktop/api/winsvc/nf-winsvc-startservicea">StartService</a> function shortly after boot, the system starts the service on demand instead of delaying its start further. If this situation is likely to occur on a regular basis, the service should not be marked as a delayed auto-start service.

If a client calls a delayed auto-start service before it is loaded, the call fails. Therefore, clients should be prepared to either retry the call or demand start the service.

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a">ChangeServiceConfig2</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfig2a">QueryServiceConfig2</a>