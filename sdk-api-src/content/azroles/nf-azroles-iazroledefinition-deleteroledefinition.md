---
UID: NF:azroles.IAzRoleDefinition.DeleteRoleDefinition
title: IAzRoleDefinition::DeleteRoleDefinition (azroles.h)
description: Removes the IAzRoleDefinition object with the specified name from this IAzRoleDefinition object.
helpviewer_keywords: ["DeleteRoleDefinition","DeleteRoleDefinition method [Security]","DeleteRoleDefinition method [Security]","IAzRoleDefinition interface","IAzRoleDefinition interface [Security]","DeleteRoleDefinition method","IAzRoleDefinition.DeleteRoleDefinition","IAzRoleDefinition::DeleteRoleDefinition","azroles/IAzRoleDefinition::DeleteRoleDefinition","security.iazroledefinition_deleteroledefinition"]
old-location: security\iazroledefinition_deleteroledefinition.htm
tech.root: security
ms.assetid: aba2f195-ebd8-40a2-8af4-455144822588
ms.date: 12/05/2018
ms.keywords: DeleteRoleDefinition, DeleteRoleDefinition method [Security], DeleteRoleDefinition method [Security],IAzRoleDefinition interface, IAzRoleDefinition interface [Security],DeleteRoleDefinition method, IAzRoleDefinition.DeleteRoleDefinition, IAzRoleDefinition::DeleteRoleDefinition, azroles/IAzRoleDefinition::DeleteRoleDefinition, security.iazroledefinition_deleteroledefinition
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
 - IAzRoleDefinition::DeleteRoleDefinition
 - azroles/IAzRoleDefinition::DeleteRoleDefinition
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
 - IAzRoleDefinition.DeleteRoleDefinition
---

# IAzRoleDefinition::DeleteRoleDefinition


## -description

The <b>DeleteRoleDefinition</b> method removes the <a href="/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object with the specified name from this <b>IAzRoleDefinition</b> object.

## -parameters

### -param bstrRoleDefinition [in]

The name of the <a href="/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object to delete.

## -returns

 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

If there are any references to an <a href="/windows/desktop/api/azroles/nn-azroles-iazroledefinition">IAzRoleDefinition</a> object that has been deleted from the cache, the <b>IAzRoleDefinition</b> object can no longer be used. In C++, you must release references to deleted <b>IAzRoleDefinition</b> objects by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.