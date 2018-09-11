---
UID: NF:taskschd.IPrincipal.get_UserId
title: IPrincipal::get_UserId
author: windows-sdk-content
description: Gets or sets the user identifier that is required to run the tasks that are associated with the principal.
old-location: taskschd\iprincipal_userid.htm
tech.root: TaskSchd
ms.assetid: b85a1f05-acb0-4b3c-bea0-393ad7c6a43d
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IPrincipal interface [Task Scheduler],UserId property, IPrincipal.UserId, IPrincipal.get_UserId, IPrincipal::UserId, IPrincipal::get_UserId, IPrincipal::put_UserId, UserId property [Task Scheduler], UserId property [Task Scheduler],IPrincipal interface, get_UserId, taskschd.iprincipal_userid, taskschd/IPrincipal::UserId, taskschd/IPrincipal::get_UserId, taskschd/IPrincipal::put_UserId
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
 - IPrincipal.UserId
 - IPrincipal.get_UserId
 - IPrincipal.put_UserId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPrincipal::get_UserId


## -description


Gets or sets the user identifier that is required to run the tasks  that are associated with the principal.

This property is read/write.


## -parameters


## -remarks



Do not set this property if a group identifier is specified in the <a href="https://msdn.microsoft.com/df4bffa3-ee38-49cd-bec7-28edda48a953">GroupId</a> property.

When reading or writing XML for a task, the user identifier for a principal is specified in the <a href="https://msdn.microsoft.com/7f3c92bf-c982-4155-9391-862f674a3665">UserId</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/df4bffa3-ee38-49cd-bec7-28edda48a953">GroupId Property of IPrincipal</a>



<a href="https://msdn.microsoft.com/7aa22af2-7f0a-41c1-89c6-d813780e89bf">IPrincipal</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

