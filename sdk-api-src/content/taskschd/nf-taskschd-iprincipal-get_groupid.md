---
UID: NF:taskschd.IPrincipal.get_GroupId
title: IPrincipal::get_GroupId
author: windows-sdk-content
description: Gets or sets the identifier of the user group that is required to run the tasks that are associated with the principal.
old-location: taskschd\iprincipal_groupid.htm
tech.root: TaskSchd
ms.assetid: df4bffa3-ee38-49cd-bec7-28edda48a953
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GroupId property [Task Scheduler], GroupId property [Task Scheduler],IPrincipal interface, IPrincipal interface [Task Scheduler],GroupId property, IPrincipal.GroupId, IPrincipal.get_GroupId, IPrincipal::GroupId, IPrincipal::get_GroupId, IPrincipal::put_GroupId, get_GroupId, taskschd.iprincipal_groupid, taskschd/IPrincipal::GroupId, taskschd/IPrincipal::get_GroupId, taskschd/IPrincipal::put_GroupId
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
 - IPrincipal.GroupId
 - IPrincipal.get_GroupId
 - IPrincipal.put_GroupId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPrincipal::get_GroupId


## -description


Gets or sets the identifier of the user group that is required to run the tasks that are associated with the principal.

This property is read/write.


## -parameters


## -remarks



Do not set this property if a user identifier is specified in the <a href="https://msdn.microsoft.com/b85a1f05-acb0-4b3c-bea0-393ad7c6a43d">UserId</a> property.

When reading or writing XML for a task, the group identifier for a principal is specified in the <a href="https://msdn.microsoft.com/1e576c31-79a9-42d4-b497-74412e464d60">GroupId</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/7aa22af2-7f0a-41c1-89c6-d813780e89bf">IPrincipal</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="https://msdn.microsoft.com/b85a1f05-acb0-4b3c-bea0-393ad7c6a43d">UserId</a>
 

 

