---
UID: NF:taskschd.IPrincipal.put_DisplayName
title: IPrincipal::put_DisplayName (taskschd.h)
description: Gets or sets the name of the principal. (Put)
helpviewer_keywords: ["DisplayName property [Task Scheduler]","DisplayName property [Task Scheduler]","IPrincipal interface","IPrincipal interface [Task Scheduler]","DisplayName property","IPrincipal.DisplayName","IPrincipal.put_DisplayName","IPrincipal::DisplayName","IPrincipal::get_DisplayName","IPrincipal::put_DisplayName","put_DisplayName","taskschd.iprincipal_displayname","taskschd/IPrincipal::DisplayName","taskschd/IPrincipal::get_DisplayName","taskschd/IPrincipal::put_DisplayName"]
old-location: taskschd\iprincipal_displayname.htm
tech.root: taskschd
ms.assetid: 285a0e64-d796-4b0d-84b1-9ebd0728ddc0
ms.date: 12/05/2018
ms.keywords: DisplayName property [Task Scheduler], DisplayName property [Task Scheduler],IPrincipal interface, IPrincipal interface [Task Scheduler],DisplayName property, IPrincipal.DisplayName, IPrincipal.put_DisplayName, IPrincipal::DisplayName, IPrincipal::get_DisplayName, IPrincipal::put_DisplayName, put_DisplayName, taskschd.iprincipal_displayname, taskschd/IPrincipal::DisplayName, taskschd/IPrincipal::get_DisplayName, taskschd/IPrincipal::put_DisplayName
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
 - IPrincipal::put_DisplayName
 - taskschd/IPrincipal::put_DisplayName
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
 - IPrincipal.DisplayName
 - IPrincipal.get_DisplayName
 - IPrincipal.put_DisplayName
---

# IPrincipal::put_DisplayName


## -description

Gets or sets the name of the principal.

This property is read/write.

## -parameters

## -remarks

When reading or writing XML for a task, the display name for a principal is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-displayname-principaltype-element">DisplayName</a> element of the Task Scheduler schema.

When setting this property value, the value can be text that is retrieved from a resource .dll file. A specialized string is used to reference the text from the resource file.  The format of the string is $(@ [Dll], [ResourceID]) where [Dll] is the path to the .dll file that contains the resource and [ResourceID] is the identifier for the resource text. For example, the setting this property value to $(@ %SystemRoot%\System32\ResourceName.dll, -101) will set the property to the value of the resource text  with an identifier equal to -101 in the  %SystemRoot%\System32\ResourceName.dll file.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iprincipal">IPrincipal</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
