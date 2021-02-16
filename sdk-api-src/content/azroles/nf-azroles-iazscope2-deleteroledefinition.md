---
UID: NF:azroles.IAzScope2.DeleteRoleDefinition
title: IAzScope2::DeleteRoleDefinition (azroles.h)
description: Removes the specified IAzRoleDefinition object from this scope.
helpviewer_keywords: ["DeleteRoleDefinition","DeleteRoleDefinition method [Security]","DeleteRoleDefinition method [Security]","IAzScope2 interface","IAzScope2 interface [Security]","DeleteRoleDefinition method","IAzScope2.DeleteRoleDefinition","IAzScope2::DeleteRoleDefinition","azroles/IAzScope2::DeleteRoleDefinition","security.iazscope2_deleteroledefinition"]
old-location: security\iazscope2_deleteroledefinition.htm
tech.root: security
ms.assetid: 12eddceb-15e2-4c9a-8372-749b0eccdd79
ms.date: 12/05/2018
ms.keywords: DeleteRoleDefinition, DeleteRoleDefinition method [Security], DeleteRoleDefinition method [Security],IAzScope2 interface, IAzScope2 interface [Security],DeleteRoleDefinition method, IAzScope2.DeleteRoleDefinition, IAzScope2::DeleteRoleDefinition, azroles/IAzScope2::DeleteRoleDefinition, security.iazscope2_deleteroledefinition
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
 - IAzScope2::DeleteRoleDefinition
 - azroles/IAzScope2::DeleteRoleDefinition
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
 - IAzScope2.DeleteRoleDefinition
---

# IAzScope2::DeleteRoleDefinition


## -description

The <b>DeleteRoleDefinition</b> method removes the specified <a href="/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object from this scope.

## -parameters

### -param bstrRoleDefinitionName [in]

A string that contains the name of the <a href="/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object to remove.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

If any references to an <a href="/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object have been deleted from the cache, that object can no longer be used. In C++, you must release references to deleted <b>IAzRoleDefinition</b> objects by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.