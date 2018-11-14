---
UID: NF:taskschd.IEmailAction.get_Attachments
title: IEmailAction::get_Attachments
author: windows-sdk-content
description: Gets or sets the pointer to an array of attachments that is sent with the email message.
old-location: taskschd\iemailaction_attachments.htm
tech.root: TaskSchd
ms.assetid: 06a3cf8f-d7fd-4ed6-9fd6-ea45face034a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Attachments property [Task Scheduler], Attachments property [Task Scheduler],IEmailAction interface, IEmailAction interface [Task Scheduler],Attachments property, IEmailAction.Attachments, IEmailAction.get_Attachments, IEmailAction::Attachments, IEmailAction::get_Attachments, IEmailAction::put_Attachments, get_Attachments, taskschd.iemailaction_attachments, taskschd/IEmailAction::Attachments, taskschd/IEmailAction::get_Attachments, taskschd/IEmailAction::put_Attachments
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: taskschd.h
req.include-header: 
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
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - IEmailAction.Attachments
 - IEmailAction.get_Attachments
 - IEmailAction.put_Attachments
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- taskschd.h
: 
- IEmailAction.get_Attachments
: 
---

# IEmailAction::get_Attachments


## -description


<p class="CCE_Message">[This interface is no longer supported. Please use IExecAction with the  powershell <a href="https://msdn.microsoft.com/library/Hh849925(v=WPS.620).aspx">Send-MailMessage</a> cmdlet as a workaround.]

Gets or sets the pointer to an array of attachments that is sent with the email message.

This property is read/write.


## -parameters


## -remarks



A maximum of eight attachments can be in the array of attachments.




## -see-also




<a href="https://msdn.microsoft.com/2f08fd42-233a-40ee-96d0-f0ac8b25b847">IEmailAction</a>
 

 

