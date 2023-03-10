---
UID: NF:azroles.IAzApplication.CreateRole
title: IAzApplication::CreateRole (azroles.h)
description: Creates an IAzRole object with the specified name. (IAzApplication.CreateRole)
helpviewer_keywords: ["AzApplication object [Security]","CreateRole method","CreateRole","CreateRole method [Security]","CreateRole method [Security]","AzApplication object","CreateRole method [Security]","IAzApplication interface","IAzApplication interface [Security]","CreateRole method","IAzApplication.CreateRole","IAzApplication::CreateRole","azroles/IAzApplication::CreateRole","security.iazapplication_createrole"]
old-location: security\iazapplication_createrole.htm
tech.root: security
ms.assetid: abad30e8-a483-4c29-ae87-4218882e8319
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],CreateRole method, CreateRole, CreateRole method [Security], CreateRole method [Security],AzApplication object, CreateRole method [Security],IAzApplication interface, IAzApplication interface [Security],CreateRole method, IAzApplication.CreateRole, IAzApplication::CreateRole, azroles/IAzApplication::CreateRole, security.iazapplication_createrole
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
 - IAzApplication::CreateRole
 - azroles/IAzApplication::CreateRole
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
 - IAzApplication.CreateRole
 - AzApplication.CreateRole
---

# IAzApplication::CreateRole


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

 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.

## -remarks

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-submit">IAzRole::Submit</a> method to persist any changes made to the returned object.

The returned <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> object is an immediate child object of the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object.
