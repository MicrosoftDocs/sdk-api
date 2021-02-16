---
UID: NF:azroles.IAzRoleDefinition.AddRoleDefinition
title: IAzRoleDefinition::AddRoleDefinition (azroles.h)
description: Adds the specified IAzRoleDefinition object to this IAzRoleDefinition object.
helpviewer_keywords: ["AddRoleDefinition","AddRoleDefinition method [Security]","AddRoleDefinition method [Security]","IAzRoleDefinition interface","IAzRoleDefinition interface [Security]","AddRoleDefinition method","IAzRoleDefinition.AddRoleDefinition","IAzRoleDefinition::AddRoleDefinition","azroles/IAzRoleDefinition::AddRoleDefinition","security.iazroledefinition_addroledefinition"]
old-location: security\iazroledefinition_addroledefinition.htm
tech.root: security
ms.assetid: 38d65f5f-452b-4641-a683-2740fb529064
ms.date: 12/05/2018
ms.keywords: AddRoleDefinition, AddRoleDefinition method [Security], AddRoleDefinition method [Security],IAzRoleDefinition interface, IAzRoleDefinition interface [Security],AddRoleDefinition method, IAzRoleDefinition.AddRoleDefinition, IAzRoleDefinition::AddRoleDefinition, azroles/IAzRoleDefinition::AddRoleDefinition, security.iazroledefinition_addroledefinition
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
 - IAzRoleDefinition::AddRoleDefinition
 - azroles/IAzRoleDefinition::AddRoleDefinition
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
 - IAzRoleDefinition.AddRoleDefinition
---

# IAzRoleDefinition::AddRoleDefinition


## -description

The <b>AddRoleDefinition</b> method adds the specified <a href="/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object to this <b>IAzRoleDefinition</b> object.

## -parameters

### -param bstrRoleDefinition [in]

The name of the <a href="/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> to add.

## -returns

 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iaztask-submit">Submit</a> method to persist any changes made by this method.