---
UID: NF:azroles.IAzScope.DeleteApplicationGroup
title: IAzScope::DeleteApplicationGroup (azroles.h)
description: Removes the IAzApplicationGroup object with the specified name from the IAzScope object.
helpviewer_keywords: ["AzScope object [Security]","DeleteApplicationGroup method","DeleteApplicationGroup","DeleteApplicationGroup method [Security]","DeleteApplicationGroup method [Security]","AzScope object","DeleteApplicationGroup method [Security]","IAzScope interface","IAzScope interface [Security]","DeleteApplicationGroup method","IAzScope.DeleteApplicationGroup","IAzScope::DeleteApplicationGroup","azroles/IAzScope::DeleteApplicationGroup","security.iazscope_deleteapplicationgroup"]
old-location: security\iazscope_deleteapplicationgroup.htm
tech.root: security
ms.assetid: 9571bff3-dfe5-48fa-be51-38d61da40414
ms.date: 12/05/2018
ms.keywords: AzScope object [Security],DeleteApplicationGroup method, DeleteApplicationGroup, DeleteApplicationGroup method [Security], DeleteApplicationGroup method [Security],AzScope object, DeleteApplicationGroup method [Security],IAzScope interface, IAzScope interface [Security],DeleteApplicationGroup method, IAzScope.DeleteApplicationGroup, IAzScope::DeleteApplicationGroup, azroles/IAzScope::DeleteApplicationGroup, security.iazscope_deleteapplicationgroup
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
 - IAzScope::DeleteApplicationGroup
 - azroles/IAzScope::DeleteApplicationGroup
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
 - IAzScope.DeleteApplicationGroup
 - AzScope.DeleteApplicationGroup
---

# IAzScope::DeleteApplicationGroup


## -description

The <b>DeleteApplicationGroup</b> method removes the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object with the specified name from the <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object.

## -parameters

### -param bstrGroupName [in]

Name of the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object to delete.

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

If there are any <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> references to an <b>IAzApplicationGroup</b> object that has been deleted from the cache, the <b>IAzApplicationGroup</b> object can no longer be used. In C++, you must release references to deleted <b>IAzApplicationGroup</b> objects by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.