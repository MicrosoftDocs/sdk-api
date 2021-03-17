---
UID: NS:winsvc._SERVICE_LAUNCH_PROTECTED_INFO
title: SERVICE_LAUNCH_PROTECTED_INFO (winsvc.h)
description: Indicates a service protection type.
helpviewer_keywords: ["*PSERVICE_LAUNCH_PROTECTED_INFO","PSERVICE_LAUNCH_PROTECTED_INFO","PSERVICE_LAUNCH_PROTECTED_INFO structure pointer","SERVICE_LAUNCH_PROTECTED_ANTIMALWARE_LIGHT","SERVICE_LAUNCH_PROTECTED_INFO","SERVICE_LAUNCH_PROTECTED_INFO structure","SERVICE_LAUNCH_PROTECTED_NONE","SERVICE_LAUNCH_PROTECTED_WINDOWS","SERVICE_LAUNCH_PROTECTED_WINDOWS_LIGHT","base.service_launch_protected_info","winsvc/PSERVICE_LAUNCH_PROTECTED_INFO","winsvc/SERVICE_LAUNCH_PROTECTED_INFO"]
old-location: base\service_launch_protected_info.htm
tech.root: security
ms.assetid: ECD44E9F-BE48-4038-94B4-37C8CA5C89F7
ms.date: 12/05/2018
ms.keywords: '*PSERVICE_LAUNCH_PROTECTED_INFO, PSERVICE_LAUNCH_PROTECTED_INFO, PSERVICE_LAUNCH_PROTECTED_INFO structure pointer, SERVICE_LAUNCH_PROTECTED_ANTIMALWARE_LIGHT, SERVICE_LAUNCH_PROTECTED_INFO, SERVICE_LAUNCH_PROTECTED_INFO structure, SERVICE_LAUNCH_PROTECTED_NONE, SERVICE_LAUNCH_PROTECTED_WINDOWS, SERVICE_LAUNCH_PROTECTED_WINDOWS_LIGHT, base.service_launch_protected_info, winsvc/PSERVICE_LAUNCH_PROTECTED_INFO, winsvc/SERVICE_LAUNCH_PROTECTED_INFO'
req.header: winsvc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: SERVICE_LAUNCH_PROTECTED_INFO, *PSERVICE_LAUNCH_PROTECTED_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVICE_LAUNCH_PROTECTED_INFO
 - winsvc/_SERVICE_LAUNCH_PROTECTED_INFO
 - PSERVICE_LAUNCH_PROTECTED_INFO
 - winsvc/PSERVICE_LAUNCH_PROTECTED_INFO
 - SERVICE_LAUNCH_PROTECTED_INFO
 - winsvc/SERVICE_LAUNCH_PROTECTED_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinSvc.h
api_name:
 - SERVICE_LAUNCH_PROTECTED_INFO
---

# SERVICE_LAUNCH_PROTECTED_INFO structure


## -description

Indicates a service protection type.

## -struct-fields

### -field dwLaunchProtected

The protection type of the service. This member can be one of the following values:



#### SERVICE_LAUNCH_PROTECTED_NONE (0)



#### SERVICE_LAUNCH_PROTECTED_WINDOWS (1)



#### SERVICE_LAUNCH_PROTECTED_WINDOWS_LIGHT (2)



#### SERVICE_LAUNCH_PROTECTED_ANTIMALWARE_LIGHT (3)

## -remarks

This structure is used by the <a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a">ChangeServiceConfig2</a> function to specify the protection type of the service, and it is used with <a href="/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfig2a">QueryServiceConfig2</a> to retrieve service configuration information for protected services. In order to apply any protection type to a service, the service must be signed with an appropriate certificate.

The <b>SERVICE_LAUNCH_PROTECTED_WINDOWS</b> and <b>SERVICE_LAUNCH_PROTECTED_WINDOWS_LIGHT</b> protection types are reserved for internal Windows use only.

The <b>SERVICE_LAUNCH_PROTECTED_ANTIMALWARE_LIGHT</b> protection type can be used by the anti-malware vendors to launch their anti-malware service as protected. See <a href="/windows/desktop/Services/protecting-anti-malware-services-">Protecting Anti-Malware Services</a> for more info.

Once the service is launched as protected, other unprotected processes will not be able to call the following APIs on the protected service.

<ul>
<li>
<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga">ChangeServiceConfig</a>
</li>
<li>
<a href="/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a">ChangeServiceConfig2</a>
</li>
<li>
<a href="/windows/desktop/api/winsvc/nf-winsvc-controlservice">ControlService</a>
</li>
<li>
<a href="/windows/desktop/api/winsvc/nf-winsvc-controlserviceexa">ControlServiceEx</a>
</li>
<li>
<a href="/windows/desktop/api/winsvc/nf-winsvc-deleteservice">DeleteService</a>
</li>
<li>
<a href="/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity">SetServiceObjectSecurity</a>
</li>
</ul>