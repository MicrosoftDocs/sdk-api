---
UID: NF:azroles.IAzScope.CreateRole
title: IAzScope::CreateRole (azroles.h)
description: Creates an IAzRole object with the specified name. (IAzScope.CreateRole)
helpviewer_keywords: ["AzScope object [Security]","CreateRole method","CreateRole","CreateRole method [Security]","CreateRole method [Security]","AzScope object","CreateRole method [Security]","IAzScope interface","IAzScope interface [Security]","CreateRole method","IAzScope.CreateRole","IAzScope::CreateRole","azroles/IAzScope::CreateRole","security.iazscope_createrole"]
old-location: security\iazscope_createrole.htm
tech.root: security
ms.assetid: a5e527f9-0aab-40d9-83fe-f19f73673266
ms.date: 12/05/2018
ms.keywords: AzScope object [Security],CreateRole method, CreateRole, CreateRole method [Security], CreateRole method [Security],AzScope object, CreateRole method [Security],IAzScope interface, IAzScope interface [Security],CreateRole method, IAzScope.CreateRole, IAzScope::CreateRole, azroles/IAzScope::CreateRole, security.iazscope_createrole
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
 - IAzScope::CreateRole
 - azroles/IAzScope::CreateRole
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
 - IAzScope.CreateRole
 - AzScope.CreateRole
---

# IAzScope::CreateRole


## -description

The <b>CreateRole</b> method creates an <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> object with the specified name.

## -parameters

### -param bstrRoleName [in]

Name for the new <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> object.

### -param varReserved [in, optional]

Reserved for future use.

### -param ppRole [out]

A pointer to a pointer to the created <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> object.

## -returns

The return value is an <b>HRESULT</b>. A value of S_OK indicates success. Any other value indicates that the operation failed.

## -remarks

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-submit">IAzRole::Submit</a> method to persist any changes made to the returned object.

The returned <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> object is an immediate child object of the <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object.
