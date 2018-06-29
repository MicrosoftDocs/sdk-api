---
UID: NS:winsvc._SERVICE_LAUNCH_PROTECTED_INFO
title: "_SERVICE_LAUNCH_PROTECTED_INFO"
author: windows-sdk-content
description: Indicates a service protection type.
old-location: base\service_launch_protected_info.htm
old-project: Services
ms.assetid: ECD44E9F-BE48-4038-94B4-37C8CA5C89F7
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: "*PSERVICE_LAUNCH_PROTECTED_INFO, PSERVICE_LAUNCH_PROTECTED_INFO, PSERVICE_LAUNCH_PROTECTED_INFO structure pointer, SERVICE_LAUNCH_PROTECTED_ANTIMALWARE_LIGHT, SERVICE_LAUNCH_PROTECTED_INFO, SERVICE_LAUNCH_PROTECTED_INFO structure, SERVICE_LAUNCH_PROTECTED_NONE, SERVICE_LAUNCH_PROTECTED_WINDOWS, SERVICE_LAUNCH_PROTECTED_WINDOWS_LIGHT, _SERVICE_LAUNCH_PROTECTED_INFO, base.service_launch_protected_info, winsvc/PSERVICE_LAUNCH_PROTECTED_INFO, winsvc/SERVICE_LAUNCH_PROTECTED_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: SERVICE_LAUNCH_PROTECTED_INFO, *PSERVICE_LAUNCH_PROTECTED_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinSvc.h
api_name:
 - SERVICE_LAUNCH_PROTECTED_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _SERVICE_LAUNCH_PROTECTED_INFO structure


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



This structure is used by the <a href="https://msdn.microsoft.com/6e5b79ed-52e1-460e-b076-01afbd08775c">ChangeServiceConfig2</a> function to specify the protection type of the service, and it is used with <a href="https://msdn.microsoft.com/cb090e59-aeff-4420-bb7c-912a4911006f">QueryServiceConfig2</a> to retrieve service configuration information for protected services. In order to apply any protection type to a service, the service must be signed with an appropriate certificate.

The <b>SERVICE_LAUNCH_PROTECTED_WINDOWS</b> and <b>SERVICE_LAUNCH_PROTECTED_WINDOWS_LIGHT</b> protection types are reserved for internal Windows use only.

The <b>SERVICE_LAUNCH_PROTECTED_ANTIMALWARE_LIGHT</b> protection type can be used by the anti-malware vendors to launch their anti-malware service as protected. See <a href="https://msdn.microsoft.com/library/Dn313124(v=VS.85).aspx">Protecting Anti-Malware Services</a> for more info.

Once the service is launched as protected, other unprotected processes will not be able to call the following APIs on the protected service.

<ul>
<li>
<a href="https://msdn.microsoft.com/add8a99b-aced-4341-9790-86efac76df6b">ChangeServiceConfig</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6e5b79ed-52e1-460e-b076-01afbd08775c">ChangeServiceConfig2</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c112b587-7455-4f15-93e1-ded73de6dbbd">ControlService</a>
</li>
<li>
<a href="https://msdn.microsoft.com/de249903-7545-4fb6-925a-aa647f862f93">ControlServiceEx</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5b0fc714-60e0-4ae3-8fa8-ace36dab2fb0">DeleteService</a>
</li>
<li>
<a href="https://msdn.microsoft.com/39481d9a-79d5-4bbf-8480-4095a34dddb6">SetServiceObjectSecurity</a>
</li>
</ul>


