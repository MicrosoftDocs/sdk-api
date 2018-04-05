---
UID: NF:taskschd.IShowMessageAction.get_MessageBody
title: IShowMessageAction::get_MessageBody method
author: windows-driver-content
description: Gets or sets the message text that is displayed in the body of the message box.
old-location: taskschd\ishowmessageaction_messagebody.htm
old-project: TaskSchd
ms.assetid: 7a9e4140-a010-4922-83d2-a063322640c6
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IShowMessageAction, IShowMessageAction interface [Task Scheduler], MessageBody property, IShowMessageAction.MessageBody, IShowMessageAction::get_MessageBody, IShowMessageAction::put_MessageBody, MessageBody property [Task Scheduler], MessageBody property [Task Scheduler], IShowMessageAction interface, get_MessageBody,IShowMessageAction.get_MessageBody, taskschd.ishowmessageaction_messagebody, taskschd/IShowMessageAction::MessageBody, taskschd/IShowMessageAction::get_MessageBody, taskschd/IShowMessageAction::put_MessageBody
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
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	IShowMessageAction.MessageBody
-	IShowMessageAction.get_MessageBody
-	IShowMessageAction.put_MessageBody
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IShowMessageAction::get_MessageBody method


## -description


<p class="CCE_Message">[This interface is no longer supported.  You can use IExecAction with the Windows scripting <a href="ae073d50-e4a4-4e23-8e46-0cb1369965e7">MsgBox function</a> to show a message in the user session.]

Gets or sets the message text that is displayed in the body of the message box.

This property is read/write.


## -parameters


## -remarks



Parameterized strings  can be used in the message text of the message box.  For more information, see the Examples section in <a href="https://msdn.microsoft.com/0bceb9d5-11f3-40a3-ba05-be896420e1db">ValueQueries</a> property of <a href="https://msdn.microsoft.com/23b7ecb9-d2bb-441a-8c93-126c833f99b9">IEventTrigger</a>.

When setting this property value, the value can be text that is retrieved from a resource .dll file. A specialized string is used to reference the text from the resource file.  The format of the string is $(@ [Dll], [ResourceID]) where [Dll] is the path to the .dll file that contains the resource and [ResourceID] is the identifier for the resource text. For example, the setting this property value to $(@ %SystemRoot%\System32\ResourceName.dll, -101) will set the property to the value of the resource text  with an identifier equal to -101 in the  %SystemRoot%\System32\ResourceName.dll file.





## -see-also




<a href="https://msdn.microsoft.com/329232de-6068-4757-b567-3ce4d2c5ba4a">IShowMessageAction</a>
 

 

