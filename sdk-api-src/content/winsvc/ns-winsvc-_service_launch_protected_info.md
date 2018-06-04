---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

The <b>SERVICE_LAUNCH_PROTECTED_ANTIMALWARE_LIGHT</b> protection type can be used by the anti-malware vendors to launch their anti-malware service as protected. See <a href="https://msdn.microsoft.com/88875a0d-9027-43f2-8411-34f9ff428fe5">Protecting Anti-Malware Services</a> for more info.

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


