---
UID: NF:azroles.IAzRole.AddOperation
title: IAzRole::AddOperation (azroles.h)
description: Adds the IAzOperation object with the specified name to the role.
helpviewer_keywords: ["AddOperation","AddOperation method [Security]","AddOperation method [Security]","AzRole object","AddOperation method [Security]","IAzRole interface","AzRole object [Security]","AddOperation method","IAzRole interface [Security]","AddOperation method","IAzRole.AddOperation","IAzRole::AddOperation","azroles/IAzRole::AddOperation","security.iazrole_addoperation"]
old-location: security\iazrole_addoperation.htm
tech.root: security
ms.assetid: 8c6d26ff-3287-4a1d-91cb-759f79ec92e5
ms.date: 12/05/2018
ms.keywords: AddOperation, AddOperation method [Security], AddOperation method [Security],AzRole object, AddOperation method [Security],IAzRole interface, AzRole object [Security],AddOperation method, IAzRole interface [Security],AddOperation method, IAzRole.AddOperation, IAzRole::AddOperation, azroles/IAzRole::AddOperation, security.iazrole_addoperation
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
 - IAzRole::AddOperation
 - azroles/IAzRole::AddOperation
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
 - IAzRole.AddOperation
 - AzRole.AddOperation
---

# IAzRole::AddOperation


## -description

The <b>AddOperation</b> method adds the <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object with the specified name to the role.

## -parameters

### -param bstrProp [in]

Name of the <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object to add to the role.

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-submit">Submit</a> method to persist any changes made by this method.