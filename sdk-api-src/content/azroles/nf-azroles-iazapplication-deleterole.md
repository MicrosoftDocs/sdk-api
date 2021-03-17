---
UID: NF:azroles.IAzApplication.DeleteRole
title: IAzApplication::DeleteRole (azroles.h)
description: Removes the IAzRole object with the specified name from the IAzApplication object.
helpviewer_keywords: ["AzApplication object [Security]","DeleteRole method","DeleteRole","DeleteRole method [Security]","DeleteRole method [Security]","AzApplication object","DeleteRole method [Security]","IAzApplication interface","IAzApplication interface [Security]","DeleteRole method","IAzApplication.DeleteRole","IAzApplication::DeleteRole","azroles/IAzApplication::DeleteRole","security.iazapplication_deleterole"]
old-location: security\iazapplication_deleterole.htm
tech.root: security
ms.assetid: c97c271a-f08c-481e-9787-61518d8cbb73
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],DeleteRole method, DeleteRole, DeleteRole method [Security], DeleteRole method [Security],AzApplication object, DeleteRole method [Security],IAzApplication interface, IAzApplication interface [Security],DeleteRole method, IAzApplication.DeleteRole, IAzApplication::DeleteRole, azroles/IAzApplication::DeleteRole, security.iazapplication_deleterole
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
 - IAzApplication::DeleteRole
 - azroles/IAzApplication::DeleteRole
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
 - IAzApplication.DeleteRole
 - AzApplication.DeleteRole
---

# IAzApplication::DeleteRole


## -description

The <b>DeleteRole</b> method removes the <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> object with the specified name from the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object.

## -parameters

### -param bstrRoleName [in]

Name of the <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> object to delete.

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

If there are any <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> references to an <b>IAzRole</b> object that has been deleted from the cache, the <b>IAzRole</b> object can no longer be used. In C++, you must release references to deleted <b>IAzRole</b> objects by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.