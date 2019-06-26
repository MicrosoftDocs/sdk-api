---
UID: NF:azroles.IAzApplication.get_Tasks
title: IAzApplication::get_Tasks (azroles.h)
author: windows-sdk-content
description: The Tasks property of IAzApplication retrieves an IAzTasks object that is used to enumerate IAzTask objects from the policy data.
old-location: security\iazapplication_tasks.htm
tech.root: SecAuthZ
ms.assetid: 86126517-d239-4ee8-a7e4-7ad5b0aac6c7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],Tasks property, IAzApplication interface [Security],Tasks property, IAzApplication.Tasks, IAzApplication.get_Tasks, IAzApplication::Tasks, IAzApplication::get_Tasks, Tasks property [Security], Tasks property [Security],AzApplication object, Tasks property [Security],IAzApplication interface, azroles/IAzApplication::Tasks, azroles/IAzApplication::get_Tasks, get_Tasks, security.iazapplication_tasks
ms.topic: method
f1_keywords: 
 - "azroles/IAzApplication.Tasks"
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
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzApplication.Tasks
 - IAzApplication.get_Tasks
 - AzApplication.Tasks
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzApplication::get_Tasks


## -description


The <b>Tasks</b> property retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iaztasks">IAzTasks</a> object that is used to enumerate <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> objects from the policy data.

This property is read-only.


## -parameters


## -remarks



This property can be used only to enumerate <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> objects that are direct child objects of the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object.



