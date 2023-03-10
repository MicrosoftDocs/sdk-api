---
UID: NF:azroles.IAzScope.CreateTask
title: IAzScope::CreateTask (azroles.h)
description: Creates an IAzTask object with the specified name. (IAzScope.CreateTask)
helpviewer_keywords: ["AzScope object [Security]","CreateTask method","CreateTask","CreateTask method [Security]","CreateTask method [Security]","AzScope object","CreateTask method [Security]","IAzScope interface","IAzScope interface [Security]","CreateTask method","IAzScope.CreateTask","IAzScope::CreateTask","azroles/IAzScope::CreateTask","security.iazscope_createtask"]
old-location: security\iazscope_createtask.htm
tech.root: security
ms.assetid: 2be1afd7-8d10-4783-a5ea-3e8c0b103ceb
ms.date: 12/05/2018
ms.keywords: AzScope object [Security],CreateTask method, CreateTask, CreateTask method [Security], CreateTask method [Security],AzScope object, CreateTask method [Security],IAzScope interface, IAzScope interface [Security],CreateTask method, IAzScope.CreateTask, IAzScope::CreateTask, azroles/IAzScope::CreateTask, security.iazscope_createtask
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
 - IAzScope::CreateTask
 - azroles/IAzScope::CreateTask
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
 - IAzScope.CreateTask
 - AzScope.CreateTask
---

# IAzScope::CreateTask


## -description

The <b>CreateTask</b> method creates an <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object with the specified name.

## -parameters

### -param bstrTaskName [in]

Name for the new <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object.

### -param varReserved [in, optional]

Reserved for future use.

### -param ppTask [out]

A pointer to a pointer to the created <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.

## -remarks

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iaztask-submit">IAzTask::Submit</a> method to persist any changes made to the returned object.

The returned <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object is an immediate child object of the <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object.
