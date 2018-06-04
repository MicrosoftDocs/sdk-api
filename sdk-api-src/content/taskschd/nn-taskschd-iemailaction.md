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

# IEmailAction interface


## -description


<p class="CCE_Message">[This interface is no longer supported. Please use IExecAction with the  powershell <a href="796227F5-C9FF-402D-8A04-CDE9E0C180EE">Send-MailMessage</a> cmdlet as a workaround.]

Represents an action that sends an email message.


## -remarks



The email action must have a valid value for the <a href="https://msdn.microsoft.com/c781f189-f27b-4f37-af53-144e1ae8cb75">Server</a>, <a href="https://msdn.microsoft.com/a0e85063-73eb-425a-a306-63ac65ab7ec8">From</a>, and <a href="https://msdn.microsoft.com/5144875a-6854-4907-89cd-6438f6adcc49">To</a> or <a href="https://msdn.microsoft.com/23493ac7-0906-4ea3-9445-3dd56c30bb13">Cc</a> properties for the task to register and run correctly.

When reading or writing your own XML for a task, an email action is specified using the <a href="https://msdn.microsoft.com/83416b02-8327-47b3-9dfc-1bf5b9365728">SendEmail</a> element of the Task Scheduler schema.

<b>Windows 8 and Windows Server 2012:  </b>This interface has been removed. Please use IExecAction with the  powershell <a href="796227F5-C9FF-402D-8A04-CDE9E0C180EE">Send-MailMessage</a> cmdlet as a workaround.


#### Examples

For more information and example code for this interface, see <a href="https://msdn.microsoft.com/cacc1b72-7c58-4117-b204-ddb3a312bb08">Event Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538787">IAction</a>



<a href="https://msdn.microsoft.com/aa7781b6-2600-4af5-95b8-2ac7928946fa">IActionCollection</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

