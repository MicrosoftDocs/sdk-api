---
UID: NF:azroles.IAzApplication.DeleteOperation
title: IAzApplication::DeleteOperation (azroles.h)
description: Removes the IAzOperation object with the specified name from the IAzApplication object.
helpviewer_keywords: ["AzApplication object [Security]","DeleteOperation method","DeleteOperation","DeleteOperation method [Security]","DeleteOperation method [Security]","AzApplication object","DeleteOperation method [Security]","IAzApplication interface","IAzApplication interface [Security]","DeleteOperation method","IAzApplication.DeleteOperation","IAzApplication::DeleteOperation","azroles/IAzApplication::DeleteOperation","security.iazapplication_deleteoperation"]
old-location: security\iazapplication_deleteoperation.htm
tech.root: security
ms.assetid: 2541e01d-20a4-424f-b8e0-5d6dedfbd7fe
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],DeleteOperation method, DeleteOperation, DeleteOperation method [Security], DeleteOperation method [Security],AzApplication object, DeleteOperation method [Security],IAzApplication interface, IAzApplication interface [Security],DeleteOperation method, IAzApplication.DeleteOperation, IAzApplication::DeleteOperation, azroles/IAzApplication::DeleteOperation, security.iazapplication_deleteoperation
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
 - IAzApplication::DeleteOperation
 - azroles/IAzApplication::DeleteOperation
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
 - IAzApplication.DeleteOperation
 - AzApplication.DeleteOperation
---

# IAzApplication::DeleteOperation


## -description

The <b>DeleteOperation</b> method removes the <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object with the specified name from the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object.

## -parameters

### -param bstrOperationName [in]

Name of the <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object to delete.

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

If there are any <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> references to an <b>IAzOperation</b> object that has been deleted from the cache, the <b>IAzOperation</b> object can no longer be used. In C++, you must release references to deleted <b>IAzOperation</b> objects by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.