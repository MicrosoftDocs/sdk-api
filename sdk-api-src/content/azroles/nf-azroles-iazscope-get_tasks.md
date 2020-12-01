---
UID: NF:azroles.IAzScope.get_Tasks
title: IAzScope::get_Tasks (azroles.h)
description: Retrieves an IAzTasks object that is used to enumerate IAzTask objects from the policy data.
helpviewer_keywords: ["AzScope object [Security]","Tasks property","IAzScope interface [Security]","Tasks property","IAzScope.Tasks","IAzScope.get_Tasks","IAzScope::Tasks","IAzScope::get_Tasks","Tasks property [Security]","Tasks property [Security]","AzScope object","Tasks property [Security]","IAzScope interface","azroles/IAzScope::Tasks","azroles/IAzScope::get_Tasks","get_Tasks","security.iazscope_tasks"]
old-location: security\iazscope_tasks.htm
tech.root: security
ms.assetid: 4b8a5280-570d-46eb-a6cb-2723cde3eb15
ms.date: 12/05/2018
ms.keywords: AzScope object [Security],Tasks property, IAzScope interface [Security],Tasks property, IAzScope.Tasks, IAzScope.get_Tasks, IAzScope::Tasks, IAzScope::get_Tasks, Tasks property [Security], Tasks property [Security],AzScope object, Tasks property [Security],IAzScope interface, azroles/IAzScope::Tasks, azroles/IAzScope::get_Tasks, get_Tasks, security.iazscope_tasks
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
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzScope::get_Tasks
 - azroles/IAzScope::get_Tasks
dev_langs:
 - c++
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
---

# IAzScope::get_Tasks


## -description

The <b>Tasks</b> property retrieves an <a href="/windows/desktop/api/azroles/nn-azroles-iaztasks">IAzTasks</a> object that is used to enumerate <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> objects from the policy data.

This property is read-only.

## -parameters

## -remarks

This property can be used only to enumerate <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> objects that are direct child objects of the <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object.