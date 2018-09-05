---
UID: NS:winsvc._SERVICE_REQUIRED_PRIVILEGES_INFOW
title: "_SERVICE_REQUIRED_PRIVILEGES_INFOW"
author: windows-sdk-content
description: Represents the required privileges for a service.
old-location: base\service_required_privileges_info.htm
old-project: Services
ms.assetid: 15a2e042-cfd5-443e-a3b8-822f48eb9654
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPSERVICE_REQUIRED_PRIVILEGES_INFOW, LPSERVICE_REQUIRED_PRIVILEGES_INFO, LPSERVICE_REQUIRED_PRIVILEGES_INFO structure pointer, SERVICE_REQUIRED_PRIVILEGES_INFO, SERVICE_REQUIRED_PRIVILEGES_INFO structure, SERVICE_REQUIRED_PRIVILEGES_INFOA, SERVICE_REQUIRED_PRIVILEGES_INFOW, _SERVICE_REQUIRED_PRIVILEGES_INFOW, base.service_required_privileges_info, winsvc/LPSERVICE_REQUIRED_PRIVILEGES_INFO, winsvc/SERVICE_REQUIRED_PRIVILEGES_INFO, winsvc/SERVICE_REQUIRED_PRIVILEGES_INFOA, winsvc/SERVICE_REQUIRED_PRIVILEGES_INFOW"
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
req.unicode-ansi: SERVICE_REQUIRED_PRIVILEGES_INFOW (Unicode) and SERVICE_REQUIRED_PRIVILEGES_INFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SERVICE_REQUIRED_PRIVILEGES_INFOW, *LPSERVICE_REQUIRED_PRIVILEGES_INFOW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsvc.h
api_name:
 - SERVICE_REQUIRED_PRIVILEGES_INFO
 - SERVICE_REQUIRED_PRIVILEGES_INFOA
 - SERVICE_REQUIRED_PRIVILEGES_INFOW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _SERVICE_REQUIRED_PRIVILEGES_INFOW structure


## -description


Represents the required privileges for a service.


## -struct-fields




### -field pmszRequiredPrivileges

A multi-string that specifies the privileges. For a list of possible values, see <a href="https://msdn.microsoft.com/973796a6-bc2e-4e64-92db-5e17b9c25460">Privilege Constants</a>.

A multi-string is a sequence of null-terminated strings, terminated by an empty string (\0). The following is an example: <code>String1\0String2\0String3\0LastString\0\0</code>.


## -remarks



The change in required privileges takes effect the next time the service is started. The SCM determines whether the service can support the specified privileges when it attempts to start the service.

It is best to analyze your service and use the minimum set of privileges required.

If you do not set the required privileges, the SCM uses all the privileges assigned by default to the process token. If you specify privileges for a service, the SCM will remove the privileges that are not required from the process token when the process starts. If multiple services share a process, the SCM computes the union of privileges required by all services in the process.

For compatibility, the SeChangeNotifyPrivilege privilege is never removed from a process token, even if no service in the process has requested the privilege. Therefore, a service need not explicitly specify this privilege.




## -see-also




<a href="https://msdn.microsoft.com/6e5b79ed-52e1-460e-b076-01afbd08775c">ChangeServiceConfig2</a>



<a href="https://msdn.microsoft.com/cb090e59-aeff-4420-bb7c-912a4911006f">QueryServiceConfig2</a>
 

 

