---
UID: NF:azroles.IAzScope2.OpenRoleDefinition
title: IAzScope2::OpenRoleDefinition (azroles.h)
description: Opens an IAzRoleDefinition object with the specified name in this scope.
helpviewer_keywords: ["IAzScope2 interface [Security]","OpenRoleDefinition method","IAzScope2.OpenRoleDefinition","IAzScope2::OpenRoleDefinition","OpenRoleDefinition","OpenRoleDefinition method [Security]","OpenRoleDefinition method [Security]","IAzScope2 interface","azroles/IAzScope2::OpenRoleDefinition","security.iazscope2_openroledefinition"]
old-location: security\iazscope2_openroledefinition.htm
tech.root: security
ms.assetid: 58b792aa-1432-4b23-8d7a-33606741bf27
ms.date: 12/05/2018
ms.keywords: IAzScope2 interface [Security],OpenRoleDefinition method, IAzScope2.OpenRoleDefinition, IAzScope2::OpenRoleDefinition, OpenRoleDefinition, OpenRoleDefinition method [Security], OpenRoleDefinition method [Security],IAzScope2 interface, azroles/IAzScope2::OpenRoleDefinition, security.iazscope2_openroledefinition
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
 - IAzScope2::OpenRoleDefinition
 - azroles/IAzScope2::OpenRoleDefinition
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
 - IAzScope2.OpenRoleDefinition
---

# IAzScope2::OpenRoleDefinition


## -description

The <b>OpenRoleDefinition</b> method opens an <a href="/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object with the specified name in this scope.

## -parameters

### -param bstrRoleDefinitionName [in]

A string that contains the name of the <a href="/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object to open.

### -param ppRoleDefinitions [out]

The address of a pointer to the <a href="/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object that this method opens.

When you have finished using the <a href="/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object, release it by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.