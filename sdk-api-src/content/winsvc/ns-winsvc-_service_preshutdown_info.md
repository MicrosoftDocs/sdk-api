---
UID: NS:winsvc._SERVICE_PRESHUTDOWN_INFO
title: "_SERVICE_PRESHUTDOWN_INFO"
author: windows-sdk-content
description: Contains preshutdown settings.
old-location: base\service_preshutdown_info.htm
old-project: Services
ms.assetid: b9d2362c-e4d7-4072-88c2-5294b3838095
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*LPSERVICE_PRESHUTDOWN_INFO, LPSERVICE_PRESHUTDOWN_INFO, LPSERVICE_PRESHUTDOWN_INFO structure pointer, SERVICE_PRESHUTDOWN_INFO, SERVICE_PRESHUTDOWN_INFO structure, _SERVICE_PRESHUTDOWN_INFO, base.service_preshutdown_info, winsvc/LPSERVICE_PRESHUTDOWN_INFO, winsvc/SERVICE_PRESHUTDOWN_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: SERVICE_PRESHUTDOWN_INFO, *LPSERVICE_PRESHUTDOWN_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsvc.h
api_name:
 - SERVICE_PRESHUTDOWN_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _SERVICE_PRESHUTDOWN_INFO structure


## -description


Contains preshutdown settings.


## -struct-fields




### -field dwPreshutdownTimeout

The time-out value, in milliseconds.


## -remarks



The default preshutdown time-out value is 180,000 milliseconds (three minutes).

After the service control manager sends the SERVICE_CONTROL_PRESHUTDOWN notification to the <a href="https://msdn.microsoft.com/bb1b863f-e29f-496f-a50e-9ea524fe8603">HandlerEx</a> function, it waits for one of the following to occur before proceeding with other shutdown actions: the specified time elapses or the service enters the SERVICE_STOPPED state. The service can continue to update its status for as long as it is in the SERVICE_STOP_PENDING state.




## -see-also




<a href="https://msdn.microsoft.com/6e5b79ed-52e1-460e-b076-01afbd08775c">ChangeServiceConfig2</a>



<a href="https://msdn.microsoft.com/cb090e59-aeff-4420-bb7c-912a4911006f">QueryServiceConfig2</a>
 

 

