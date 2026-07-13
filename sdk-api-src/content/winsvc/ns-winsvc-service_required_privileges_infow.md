---
UID: NS:winsvc._SERVICE_REQUIRED_PRIVILEGES_INFOW
title: SERVICE_REQUIRED_PRIVILEGES_INFOW (winsvc.h)
description: Represents the required privileges for a service. (Unicode)
helpviewer_keywords: ["*LPSERVICE_REQUIRED_PRIVILEGES_INFOW","LPSERVICE_REQUIRED_PRIVILEGES_INFO","LPSERVICE_REQUIRED_PRIVILEGES_INFO structure pointer","SERVICE_REQUIRED_PRIVILEGES_INFO","SERVICE_REQUIRED_PRIVILEGES_INFO structure","SERVICE_REQUIRED_PRIVILEGES_INFOA","SERVICE_REQUIRED_PRIVILEGES_INFOW","base.service_required_privileges_info","winsvc/LPSERVICE_REQUIRED_PRIVILEGES_INFO","winsvc/SERVICE_REQUIRED_PRIVILEGES_INFO","winsvc/SERVICE_REQUIRED_PRIVILEGES_INFOA","winsvc/SERVICE_REQUIRED_PRIVILEGES_INFOW"]
old-location: base\service_required_privileges_info.htm
tech.root: security
ms.assetid: 15a2e042-cfd5-443e-a3b8-822f48eb9654
ms.date: 12/05/2018
ms.keywords: '*LPSERVICE_REQUIRED_PRIVILEGES_INFOW, LPSERVICE_REQUIRED_PRIVILEGES_INFO, LPSERVICE_REQUIRED_PRIVILEGES_INFO structure pointer, SERVICE_REQUIRED_PRIVILEGES_INFO, SERVICE_REQUIRED_PRIVILEGES_INFO structure, SERVICE_REQUIRED_PRIVILEGES_INFOA, SERVICE_REQUIRED_PRIVILEGES_INFOW, base.service_required_privileges_info, winsvc/LPSERVICE_REQUIRED_PRIVILEGES_INFO, winsvc/SERVICE_REQUIRED_PRIVILEGES_INFO, winsvc/SERVICE_REQUIRED_PRIVILEGES_INFOA, winsvc/SERVICE_REQUIRED_PRIVILEGES_INFOW'
req.header: winsvc.h
req.include-header: Windows.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SERVICE_REQUIRED_PRIVILEGES_INFOW, *LPSERVICE_REQUIRED_PRIVILEGES_INFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVICE_REQUIRED_PRIVILEGES_INFOW
 - winsvc/_SERVICE_REQUIRED_PRIVILEGES_INFOW
 - LPSERVICE_REQUIRED_PRIVILEGES_INFOW
 - winsvc/LPSERVICE_REQUIRED_PRIVILEGES_INFOW
 - SERVICE_REQUIRED_PRIVILEGES_INFOW
 - winsvc/SERVICE_REQUIRED_PRIVILEGES_INFOW
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
 - SERVICE_REQUIRED_PRIVILEGES_INFO
 - SERVICE_REQUIRED_PRIVILEGES_INFOA
 - SERVICE_REQUIRED_PRIVILEGES_INFOW
---

# SERVICE_REQUIRED_PRIVILEGES_INFOW structure


## -description

Represents the required privileges for a service.

## -struct-fields

### -field pmszRequiredPrivileges

A multi-string that specifies the privileges. For a list of possible values, see <a href="/windows/desktop/SecAuthZ/privilege-constants">Privilege Constants</a>.

A multi-string is a sequence of null-terminated strings, terminated by an empty string (\0). The following is an example: <code>String1\0String2\0String3\0LastString\0\0</code>.

## -remarks

The change in required privileges takes effect the next time the service is started. The SCM determines whether the service can support the specified privileges when it attempts to start the service.

It is best to analyze your service and use the minimum set of privileges required.

If you do not set the required privileges, the SCM uses all the privileges assigned by default to the process token. If you specify privileges for a service, the SCM will remove the privileges that are not required from the process token when the process starts. If multiple services share a process, the SCM computes the union of privileges required by all services in the process.

For compatibility, the SeChangeNotifyPrivilege privilege is never removed from a process token, even if no service in the process has requested the privilege. Therefore, a service need not explicitly specify this privilege.





> [!NOTE]
> The winsvc.h header defines SERVICE_REQUIRED_PRIVILEGES_INFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a">ChangeServiceConfig2</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfig2a">QueryServiceConfig2</a>
