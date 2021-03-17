---
UID: NF:azroles.IAzApplication3.CreateRoleDefinition
title: IAzApplication3::CreateRoleDefinition (azroles.h)
description: Creates a new IAzRoleDefinition object with the specified name.
helpviewer_keywords: ["CreateRoleDefinition","CreateRoleDefinition method [Security]","CreateRoleDefinition method [Security]","IAzApplication3 interface","IAzApplication3 interface [Security]","CreateRoleDefinition method","IAzApplication3.CreateRoleDefinition","IAzApplication3::CreateRoleDefinition","azroles/IAzApplication3::CreateRoleDefinition","security.iazapplication3_createroledefinition"]
old-location: security\iazapplication3_createroledefinition.htm
tech.root: security
ms.assetid: 014410be-4b2c-452b-b671-0a9bd9c0a448
ms.date: 12/05/2018
ms.keywords: CreateRoleDefinition, CreateRoleDefinition method [Security], CreateRoleDefinition method [Security],IAzApplication3 interface, IAzApplication3 interface [Security],CreateRoleDefinition method, IAzApplication3.CreateRoleDefinition, IAzApplication3::CreateRoleDefinition, azroles/IAzApplication3::CreateRoleDefinition, security.iazapplication3_createroledefinition
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAzApplication3::CreateRoleDefinition
 - azroles/IAzApplication3::CreateRoleDefinition
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
 - IAzApplication3.CreateRoleDefinition
---

# IAzApplication3::CreateRoleDefinition


## -description

The <b>CreateRoleDefinition</b> method creates a new <a href="/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object with the specified name.

## -parameters

### -param bstrRoleDefinitionName [in]

A string that contains the name of the new <a href="/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object.

### -param ppRoleDefinitions [out]

The address of a pointer to the <a href="/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object that this method creates.

When you have finished using this <a href="/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object, release it by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.