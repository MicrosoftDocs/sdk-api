---
UID: NF:taskschd.IShowMessageAction.put_Title
title: IShowMessageAction::put_Title (taskschd.h)
author: windows-sdk-content
description: Gets or sets the title of the message box.
old-location: taskschd\ishowmessageaction_title.htm
tech.root: taskschd
ms.assetid: 6ec51ebb-5aa3-4338-bc88-dd8df34d59ac
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IShowMessageAction interface [Task Scheduler],Title property, IShowMessageAction.Title, IShowMessageAction.put_Title, IShowMessageAction::Title, IShowMessageAction::get_Title, IShowMessageAction::put_Title, Title property [Task Scheduler], Title property [Task Scheduler],IShowMessageAction interface, put_Title, taskschd.ishowmessageaction_title, taskschd/IShowMessageAction::Title, taskschd/IShowMessageAction::get_Title, taskschd/IShowMessageAction::put_Title
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
 - IShowMessageAction.Title
 - IShowMessageAction.get_Title
 - IShowMessageAction.put_Title
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShowMessageAction::put_Title


## -description


<p class="CCE_Message">[This interface is no longer supported.  You can use IExecAction with the Windows scripting <a href="https://msdn.microsoft.com/library/sfw6660x(v=VS.85).aspx">MsgBox function</a> to show a message in the user session.]

Gets or sets the title of the message box.

This property is read/write.


## -parameters


## -remarks



Parameterized strings  can be used in the title text of the message box.  For more information, see the Examples section in <a href="https://msdn.microsoft.com/0bceb9d5-11f3-40a3-ba05-be896420e1db">ValueQueries</a> property of <a href="https://msdn.microsoft.com/23b7ecb9-d2bb-441a-8c93-126c833f99b9">IEventTrigger</a>.

When setting this property value, the value can be text that is retrieved from a resource .dll file. A specialized string is used to reference the text from the resource file.  The format of the string is $(@ [Dll], [ResourceID]) where [Dll] is the path to the .dll file that contains the resource and [ResourceID] is the identifier for the resource text. For example, the setting this property value to $(@ %SystemRoot%\System32\ResourceName.dll, -101) will set the property to the value of the resource text  with an identifier equal to -101 in the  %SystemRoot%\System32\ResourceName.dll file.





## -see-also




<a href="https://msdn.microsoft.com/329232de-6068-4757-b567-3ce4d2c5ba4a">IShowMessageAction</a>
 

 

