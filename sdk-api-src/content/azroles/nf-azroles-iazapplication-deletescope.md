---
UID: NF:azroles.IAzApplication.DeleteScope
title: IAzApplication::DeleteScope (azroles.h)
description: Removes the IAzScope object with the specified name from the IAzApplication object.
helpviewer_keywords: ["AzApplication object [Security]","DeleteScope method","DeleteScope","DeleteScope method [Security]","DeleteScope method [Security]","AzApplication object","DeleteScope method [Security]","IAzApplication interface","IAzApplication interface [Security]","DeleteScope method","IAzApplication.DeleteScope","IAzApplication::DeleteScope","azroles/IAzApplication::DeleteScope","security.iazapplication_deletescope"]
old-location: security\iazapplication_deletescope.htm
tech.root: security
ms.assetid: 2a3c2e18-9264-496a-9bd3-ff9c529a2426
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],DeleteScope method, DeleteScope, DeleteScope method [Security], DeleteScope method [Security],AzApplication object, DeleteScope method [Security],IAzApplication interface, IAzApplication interface [Security],DeleteScope method, IAzApplication.DeleteScope, IAzApplication::DeleteScope, azroles/IAzApplication::DeleteScope, security.iazapplication_deletescope
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
 - IAzApplication::DeleteScope
 - azroles/IAzApplication::DeleteScope
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
 - IAzApplication.DeleteScope
 - AzApplication.DeleteScope
---

# IAzApplication::DeleteScope


## -description

The <b>DeleteScope</b> method removes the <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object with the specified name from the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object.

## -parameters

### -param bstrScopeName [in]

Name of the <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object to delete.

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

If there are any <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> references to an <b>IAzScope</b> object that has been deleted from the cache, the <b>IAzScope</b> object can no longer be used. In C++, you must release references to deleted <b>IAzScope</b> objects by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.