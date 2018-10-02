---
UID: NF:azroles.IAzScope.get_Tasks
title: IAzScope::get_Tasks
author: windows-sdk-content
description: Retrieves an IAzTasks object that is used to enumerate IAzTask objects from the policy data.
old-location: security\iazscope_tasks.htm
tech.root: SecAuthZ
ms.assetid: 4b8a5280-570d-46eb-a6cb-2723cde3eb15
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AzScope object [Security],Tasks property, IAzScope interface [Security],Tasks property, IAzScope.Tasks, IAzScope.get_Tasks, IAzScope::Tasks, IAzScope::get_Tasks, Tasks property [Security], Tasks property [Security],AzScope object, Tasks property [Security],IAzScope interface, azroles/IAzScope::Tasks, azroles/IAzScope::get_Tasks, get_Tasks, security.iazscope_tasks
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IAzScope.Tasks
 - IAzScope.get_Tasks
 - AzScope.Tasks
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzScope::get_Tasks


## -description


The <b>Tasks</b> property retrieves an <a href="https://msdn.microsoft.com/324dec16-3fd6-4289-ba15-002e8626dec8">IAzTasks</a> object that is used to enumerate <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> objects from the policy data.

This property is read-only.


## -parameters


## -remarks



This property can be used only to enumerate <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> objects that are direct child objects of the <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object.



