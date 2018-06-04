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

# IPrincipal interface


## -description


Provides the security credentials  for a principal. These security credentials define the security context for the tasks that are associated with the principal.


## -remarks



When specifying an account, remember to properly use the double backslash in code to specify the domain and user name. For example, use DOMAIN\\UserName to specify a value for the <a href="https://msdn.microsoft.com/b85a1f05-acb0-4b3c-bea0-393ad7c6a43d">UserId</a> property.

When reading or writing XML for a task, the security credentials for a principal are specified in the <a href="https://msdn.microsoft.com/4ba65976-98d2-4329-80f0-566fac2e9fda">Principal</a> element of the Task Scheduler schema.

If a task is registered using the at.exe command line tool, and this interface is used to retrieve information about the task, then the <a href="https://msdn.microsoft.com/cf0a8ad4-f1bb-46a2-ae92-d00e08b8d459">LogonType</a> property will return 0, the <a href="https://msdn.microsoft.com/90f2dcfc-4704-4731-9b86-12a2a6f208f4">RunLevel</a> property will return 0, and the <a href="https://msdn.microsoft.com/b85a1f05-acb0-4b3c-bea0-393ad7c6a43d">UserId</a> property will return <b>NULL</b>.


#### Examples

For more information and example code for this interface, see <a href="https://msdn.microsoft.com/e45b18b0-5a7f-4283-b42f-15e9ffcfaff7">Time Trigger Example (C++)</a> or <a href="https://msdn.microsoft.com/5e2e8fa6-66c7-4356-8fd6-22f7974791b9">Registration Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3787ed9b-9fd0-473b-9034-ade97dc330d9">ITaskDefinition</a>



<a href="https://msdn.microsoft.com/d1c8389b-149c-4fcb-972a-b25fa0d8d763">Principal Property of ITaskDefinition</a>



<a href="task_scheduler_interfaces.htm">Task Scheduler Interfaces</a>
 

 

