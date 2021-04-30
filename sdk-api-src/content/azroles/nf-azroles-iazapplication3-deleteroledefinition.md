---
UID: NF:azroles.IAzApplication3.DeleteRoleDefinition
title: IAzApplication3::DeleteRoleDefinition (azroles.h)
description: Removes the specified IAzRoleDefinition object from the IAzApplication3 object.
helpviewer_keywords: ["DeleteRoleDefinition","DeleteRoleDefinition method [Security]","DeleteRoleDefinition method [Security]","IAzApplication3 interface","IAzApplication3 interface [Security]","DeleteRoleDefinition method","IAzApplication3.DeleteRoleDefinition","IAzApplication3::DeleteRoleDefinition","azroles/IAzApplication3::DeleteRoleDefinition","security.iazapplication3_deleteroledefinition"]
old-location: security\iazapplication3_deleteroledefinition.htm
tech.root: security
ms.assetid: 34dc0bb8-1a44-418a-9b2c-f506f21f6ab1
ms.date: 12/05/2018
ms.keywords: DeleteRoleDefinition, DeleteRoleDefinition method [Security], DeleteRoleDefinition method [Security],IAzApplication3 interface, IAzApplication3 interface [Security],DeleteRoleDefinition method, IAzApplication3.DeleteRoleDefinition, IAzApplication3::DeleteRoleDefinition, azroles/IAzApplication3::DeleteRoleDefinition, security.iazapplication3_deleteroledefinition
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
 - IAzApplication3::DeleteRoleDefinition
 - azroles/IAzApplication3::DeleteRoleDefinition
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
 - IAzApplication3.DeleteRoleDefinition
---

# IAzApplication3::DeleteRoleDefinition


## -description

The <b>DeleteRoleDefinition</b> method removes the specified <a href="/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object from the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication3">IAzApplication3</a> object.

## -parameters

### -param bstrRoleDefinitionName [in]

A string that contains the name of the <a href="/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object to remove.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

If any references to an <a href="/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object have been deleted from the cache, you can no longer use that object. In C++, you must release references to deleted <b>IAzRoleDefinition</b> objects by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.