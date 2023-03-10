---
UID: NN:taskschd.IPrincipal
title: IPrincipal (taskschd.h)
description: Provides the security credentials for a principal.
helpviewer_keywords: ["IPrincipal","IPrincipal interface [Task Scheduler]","IPrincipal interface [Task Scheduler]","described","taskschd.iprincipal","taskschd/IPrincipal"]
old-location: taskschd\iprincipal.htm
tech.root: taskschd
ms.assetid: 7aa22af2-7f0a-41c1-89c6-d813780e89bf
ms.date: 12/05/2018
ms.keywords: IPrincipal, IPrincipal interface [Task Scheduler], IPrincipal interface [Task Scheduler],described, taskschd.iprincipal, taskschd/IPrincipal
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
 - IPrincipal
 - taskschd/IPrincipal
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
 - IPrincipal
---

# IPrincipal interface


## -description

Provides the security credentials  for a principal. These security credentials define the security context for the tasks that are associated with the principal.

## -remarks

When specifying an account, remember to properly use the double backslash in code to specify the domain and user name. For example, use DOMAIN\\UserName to specify a value for the <a href="/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid">UserId</a> property.

When reading or writing XML for a task, the security credentials for a principal are specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-principal-principaltype-element">Principal</a> element of the Task Scheduler schema.

If a task is registered using the at.exe command line tool, and this interface is used to retrieve information about the task, then the <a href="/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype">LogonType</a> property will return 0, the <a href="/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel">RunLevel</a> property will return 0, and the <a href="/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid">UserId</a> property will return <b>NULL</b>.


#### Examples

For more information and example code for this interface, see <a href="/windows/desktop/TaskSchd/time-trigger-example--c---">Time Trigger Example (C++)</a> or <a href="/windows/desktop/TaskSchd/registration-trigger-example--c---">Registration Trigger Example (C++)</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition">ITaskDefinition</a>



<a href="/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal">Principal Property of ITaskDefinition</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>