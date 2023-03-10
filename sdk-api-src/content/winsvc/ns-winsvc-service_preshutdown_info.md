---
UID: NS:winsvc._SERVICE_PRESHUTDOWN_INFO
title: SERVICE_PRESHUTDOWN_INFO (winsvc.h)
description: Contains preshutdown settings.
helpviewer_keywords: ["*LPSERVICE_PRESHUTDOWN_INFO","LPSERVICE_PRESHUTDOWN_INFO","LPSERVICE_PRESHUTDOWN_INFO structure pointer","SERVICE_PRESHUTDOWN_INFO","SERVICE_PRESHUTDOWN_INFO structure","base.service_preshutdown_info","winsvc/LPSERVICE_PRESHUTDOWN_INFO","winsvc/SERVICE_PRESHUTDOWN_INFO"]
old-location: base\service_preshutdown_info.htm
tech.root: security
ms.assetid: b9d2362c-e4d7-4072-88c2-5294b3838095
ms.date: 12/05/2018
ms.keywords: '*LPSERVICE_PRESHUTDOWN_INFO, LPSERVICE_PRESHUTDOWN_INFO, LPSERVICE_PRESHUTDOWN_INFO structure pointer, SERVICE_PRESHUTDOWN_INFO, SERVICE_PRESHUTDOWN_INFO structure, base.service_preshutdown_info, winsvc/LPSERVICE_PRESHUTDOWN_INFO, winsvc/SERVICE_PRESHUTDOWN_INFO'
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
req.typenames: SERVICE_PRESHUTDOWN_INFO, *LPSERVICE_PRESHUTDOWN_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVICE_PRESHUTDOWN_INFO
 - winsvc/_SERVICE_PRESHUTDOWN_INFO
 - LPSERVICE_PRESHUTDOWN_INFO
 - winsvc/LPSERVICE_PRESHUTDOWN_INFO
 - SERVICE_PRESHUTDOWN_INFO
 - winsvc/SERVICE_PRESHUTDOWN_INFO
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
 - SERVICE_PRESHUTDOWN_INFO
---

# SERVICE_PRESHUTDOWN_INFO structure


## -description

Contains preshutdown settings.

## -struct-fields

### -field dwPreshutdownTimeout

The time-out value, in milliseconds.

## -remarks

Starting with the Windows Creator’s Update (build 15063) the default preshutdown time-out value is 10,000 milliseconds (10 seconds). In prior releases, the default preshutdown time-out value is 180,000 milliseconds (three minutes).

After the service control manager sends the SERVICE_CONTROL_PRESHUTDOWN notification to the <a href="/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex">HandlerEx</a> function, it waits for one of the following to occur before proceeding with other shutdown actions: the specified time elapses or the service enters the SERVICE_STOPPED state. The service can continue to update its status for as long as it is in the SERVICE_STOP_PENDING state.

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a">ChangeServiceConfig2</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfig2a">QueryServiceConfig2</a>