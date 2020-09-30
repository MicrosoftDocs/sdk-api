---
UID: NF:azroles.IAzRole.AddTask
title: IAzRole::AddTask (azroles.h)
description: Adds the IAzTask object with the specified name to the role.
helpviewer_keywords: ["AddTask","AddTask method [Security]","AddTask method [Security]","AzRole object","AddTask method [Security]","IAzRole interface","AzRole object [Security]","AddTask method","IAzRole interface [Security]","AddTask method","IAzRole.AddTask","IAzRole::AddTask","azroles/IAzRole::AddTask","security.iazrole_addtask"]
old-location: security\iazrole_addtask.htm
tech.root: security
ms.assetid: 51ba30c3-8067-4aca-b8aa-8e64d4427b98
ms.date: 12/05/2018
ms.keywords: AddTask, AddTask method [Security], AddTask method [Security],AzRole object, AddTask method [Security],IAzRole interface, AzRole object [Security],AddTask method, IAzRole interface [Security],AddTask method, IAzRole.AddTask, IAzRole::AddTask, azroles/IAzRole::AddTask, security.iazrole_addtask
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
 - IAzRole::AddTask
 - azroles/IAzRole::AddTask
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
 - IAzRole.AddTask
 - AzRole.AddTask
---

# IAzRole::AddTask


## -description

The <b>AddTask</b> method adds the <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object with the specified name to the role.

## -parameters

### -param bstrProp [in]

Name of the <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object to add to the role.

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-submit">Submit</a> method to persist any changes made by this method.