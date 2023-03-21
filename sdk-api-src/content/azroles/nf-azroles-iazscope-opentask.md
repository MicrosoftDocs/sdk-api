---
UID: NF:azroles.IAzScope.OpenTask
title: IAzScope::OpenTask (azroles.h)
description: Opens an IAzTask object with the specified name. (IAzScope.OpenTask)
helpviewer_keywords: ["AzScope object [Security]","OpenTask method","IAzScope interface [Security]","OpenTask method","IAzScope.OpenTask","IAzScope::OpenTask","OpenTask","OpenTask method [Security]","OpenTask method [Security]","AzScope object","OpenTask method [Security]","IAzScope interface","azroles/IAzScope::OpenTask","security.iazscope_opentask"]
old-location: security\iazscope_opentask.htm
tech.root: security
ms.assetid: 8719ab1f-8004-4d5c-b64c-ae17c8d1ab30
ms.date: 12/05/2018
ms.keywords: AzScope object [Security],OpenTask method, IAzScope interface [Security],OpenTask method, IAzScope.OpenTask, IAzScope::OpenTask, OpenTask, OpenTask method [Security], OpenTask method [Security],AzScope object, OpenTask method [Security],IAzScope interface, azroles/IAzScope::OpenTask, security.iazscope_opentask
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
 - IAzScope::OpenTask
 - azroles/IAzScope::OpenTask
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
 - IAzScope.OpenTask
 - AzScope.OpenTask
---

# IAzScope::OpenTask


## -description

The <b>OpenTask</b> method opens an <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object with the specified name.

## -parameters

### -param bstrTaskName [in]

Name of the <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object to open.

### -param varReserved [in, optional]

Reserved for future use.

### -param ppTask [out]

A pointer to a pointer to the opened <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.
