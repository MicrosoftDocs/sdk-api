---
UID: NF:azroles.IAzTask.get_Tasks
title: IAzTask::get_Tasks
author: windows-sdk-content
description: Retrieves the tasks associated with the task.
old-location: security\iaztask_tasks.htm
old-project: secauthz
ms.assetid: a4baa899-78eb-4a3b-bcc1-0b8c2831b10f
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: AzTask object [Security],Tasks property, IAzTask interface [Security],Tasks property, IAzTask.Tasks, IAzTask.get_Tasks, IAzTask::Tasks, IAzTask::get_Tasks, Tasks property [Security], Tasks property [Security],AzTask object, Tasks property [Security],IAzTask interface, azroles/IAzTask::Tasks, azroles/IAzTask::get_Tasks, get_Tasks, security.iaztask_tasks
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzTask.Tasks
 - IAzTask.get_Tasks
 - AzTask.Tasks
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzTask::get_Tasks


## -description


The <b>Tasks</b> property retrieves the tasks associated with the task.

This property is read-only.


## -parameters


## -remarks



This property shows the nesting of <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> objects within another <b>IAzTask</b> object.

In  JScript, the returned <a href="9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a> must be converted to the JScript <a href="08e5f552-0797-4b48-8164-609582fc18c9">Array</a> object. 



