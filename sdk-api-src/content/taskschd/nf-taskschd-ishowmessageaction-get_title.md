---
UID: NF:taskschd.IShowMessageAction.get_Title
title: IShowMessageAction::get_Title (taskschd.h)
description: Gets or sets the title of the message box. (Get)
helpviewer_keywords: ["IShowMessageAction interface [Task Scheduler]","Title property","IShowMessageAction.Title","IShowMessageAction.get_Title","IShowMessageAction::Title","IShowMessageAction::get_Title","IShowMessageAction::put_Title","Title property [Task Scheduler]","Title property [Task Scheduler]","IShowMessageAction interface","get_Title","taskschd.ishowmessageaction_title","taskschd/IShowMessageAction::Title","taskschd/IShowMessageAction::get_Title","taskschd/IShowMessageAction::put_Title"]
old-location: taskschd\ishowmessageaction_title.htm
tech.root: taskschd
ms.assetid: 6ec51ebb-5aa3-4338-bc88-dd8df34d59ac
ms.date: 12/05/2018
ms.keywords: IShowMessageAction interface [Task Scheduler],Title property, IShowMessageAction.Title, IShowMessageAction.get_Title, IShowMessageAction::Title, IShowMessageAction::get_Title, IShowMessageAction::put_Title, Title property [Task Scheduler], Title property [Task Scheduler],IShowMessageAction interface, get_Title, taskschd.ishowmessageaction_title, taskschd/IShowMessageAction::Title, taskschd/IShowMessageAction::get_Title, taskschd/IShowMessageAction::put_Title
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
 - IShowMessageAction::get_Title
 - taskschd/IShowMessageAction::get_Title
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
 - IShowMessageAction.Title
 - IShowMessageAction.get_Title
 - IShowMessageAction.put_Title
---

# IShowMessageAction::get_Title


## -description

<p class="CCE_Message">[This interface is no longer supported.  You can use IExecAction with the Windows scripting <a href="/previous-versions/sfw6660x(v=vs.85)">MsgBox function</a> to show a message in the user session.]

Gets or sets the title of the message box.

This property is read/write.

## -parameters

## -remarks

Parameterized strings  can be used in the title text of the message box.  For more information, see the Examples section in <a href="/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_valuequeries">ValueQueries</a> property of <a href="/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger">IEventTrigger</a>.

When setting this property value, the value can be text that is retrieved from a resource .dll file. A specialized string is used to reference the text from the resource file.  The format of the string is $(@ [Dll], [ResourceID]) where [Dll] is the path to the .dll file that contains the resource and [ResourceID] is the identifier for the resource text. For example, the setting this property value to $(@ %SystemRoot%\System32\ResourceName.dll, -101) will set the property to the value of the resource text  with an identifier equal to -101 in the  %SystemRoot%\System32\ResourceName.dll file.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction">IShowMessageAction</a>
