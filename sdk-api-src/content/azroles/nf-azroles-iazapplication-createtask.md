---
UID: NF:azroles.IAzApplication.CreateTask
title: IAzApplication::CreateTask (azroles.h)
description: Creates an IAzTask object with the specified name. (IAzApplication.CreateTask)
helpviewer_keywords: ["AzApplication object [Security]","CreateTask method","CreateTask","CreateTask method [Security]","CreateTask method [Security]","AzApplication object","CreateTask method [Security]","IAzApplication interface","IAzApplication interface [Security]","CreateTask method","IAzApplication.CreateTask","IAzApplication::CreateTask","azroles/IAzApplication::CreateTask","security.iazapplication_createtask"]
old-location: security\iazapplication_createtask.htm
tech.root: security
ms.assetid: 9c15f1aa-f0d7-4c6b-8c3c-b6537f7dac90
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],CreateTask method, CreateTask, CreateTask method [Security], CreateTask method [Security],AzApplication object, CreateTask method [Security],IAzApplication interface, IAzApplication interface [Security],CreateTask method, IAzApplication.CreateTask, IAzApplication::CreateTask, azroles/IAzApplication::CreateTask, security.iazapplication_createtask
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
 - IAzApplication::CreateTask
 - azroles/IAzApplication::CreateTask
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
 - IAzApplication.CreateTask
 - AzApplication.CreateTask
---

# IAzApplication::CreateTask


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

 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.

## -remarks

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iaztask-submit">IAzTask::Submit</a> method to persist any changes made to the returned object.

The returned <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object is an immediate child object of the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object.
