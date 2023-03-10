---
UID: NF:taskschd.IShowMessageAction.put_MessageBody
title: IShowMessageAction::put_MessageBody (taskschd.h)
description: Gets or sets the message text that is displayed in the body of the message box. (Put)
helpviewer_keywords: ["IShowMessageAction interface [Task Scheduler]","MessageBody property","IShowMessageAction.MessageBody","IShowMessageAction.put_MessageBody","IShowMessageAction::MessageBody","IShowMessageAction::get_MessageBody","IShowMessageAction::put_MessageBody","MessageBody property [Task Scheduler]","MessageBody property [Task Scheduler]","IShowMessageAction interface","put_MessageBody","taskschd.ishowmessageaction_messagebody","taskschd/IShowMessageAction::MessageBody","taskschd/IShowMessageAction::get_MessageBody","taskschd/IShowMessageAction::put_MessageBody"]
old-location: taskschd\ishowmessageaction_messagebody.htm
tech.root: taskschd
ms.assetid: 7a9e4140-a010-4922-83d2-a063322640c6
ms.date: 12/05/2018
ms.keywords: IShowMessageAction interface [Task Scheduler],MessageBody property, IShowMessageAction.MessageBody, IShowMessageAction.put_MessageBody, IShowMessageAction::MessageBody, IShowMessageAction::get_MessageBody, IShowMessageAction::put_MessageBody, MessageBody property [Task Scheduler], MessageBody property [Task Scheduler],IShowMessageAction interface, put_MessageBody, taskschd.ishowmessageaction_messagebody, taskschd/IShowMessageAction::MessageBody, taskschd/IShowMessageAction::get_MessageBody, taskschd/IShowMessageAction::put_MessageBody
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShowMessageAction::put_MessageBody
 - taskschd/IShowMessageAction::put_MessageBody
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - IShowMessageAction.MessageBody
 - IShowMessageAction.get_MessageBody
 - IShowMessageAction.put_MessageBody
---

# IShowMessageAction::put_MessageBody


## -description

<p class="CCE_Message">[This interface is no longer supported.  You can use IExecAction with the Windows scripting <a href="/previous-versions/sfw6660x(v=vs.85)">MsgBox function</a> to show a message in the user session.]

Gets or sets the message text that is displayed in the body of the message box.

This property is read/write.

## -parameters

## -remarks

Parameterized strings  can be used in the message text of the message box.  For more information, see the Examples section in <a href="/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries">ValueQueries</a> property of <a href="/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger">IEventTrigger</a>.

When setting this property value, the value can be text that is retrieved from a resource .dll file. A specialized string is used to reference the text from the resource file.  The format of the string is $(@ [Dll], [ResourceID]) where [Dll] is the path to the .dll file that contains the resource and [ResourceID] is the identifier for the resource text. For example, the setting this property value to $(@ %SystemRoot%\System32\ResourceName.dll, -101) will set the property to the value of the resource text  with an identifier equal to -101 in the  %SystemRoot%\System32\ResourceName.dll file.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction">IShowMessageAction</a>
