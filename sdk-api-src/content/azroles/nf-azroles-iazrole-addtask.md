---
UID: NF:azroles.IAzRole.AddTask
title: IAzRole::AddTask (azroles.h)
description: Adds the IAzTask object with the specified name to the role.
helpviewer_keywords: ["AddTask","AddTask method [Security]","AddTask method [Security]","AzRole object","AddTask method [Security]","IAzRole interface","AzRole object [Security]","AddTask method","IAzRole interface [Security]","AddTask method","IAzRole.AddTask","IAzRole::AddTask","azroles/IAzRole::AddTask","security.iazrole_addtask"]
old-location: security\iazrole_addtask.htm
tech.root: security
ms.assetid: 51ba30c3-8067-4aca-b8aa-8e64d4427b98
ms.date: 03/20/2023
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

The **AddTask** method adds the [IAzTask](nn-azroles-iaztask.md) object with the specified name to the role.

## -parameters

### -param bstrProp [in]

Name of the [IAzTask](nn-azroles-iaztask.md) object to add to the role.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

You must call the [Submit](nf-azroles-iazrole-submit.md) method to persist any changes made by this method.

## -see-also

[IAzTask](nn-azroles-iaztask.md)

[Submit](nf-azroles-iazrole-submit.md)
