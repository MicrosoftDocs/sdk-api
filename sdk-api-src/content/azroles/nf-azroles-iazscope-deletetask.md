---
UID: NF:azroles.IAzScope.DeleteTask
title: IAzScope::DeleteTask (azroles.h)
description: Removes the IAzTask object with the specified name from the IAzScope object.
helpviewer_keywords: ["AzScope object [Security]","DeleteTask method","DeleteTask","DeleteTask method [Security]","DeleteTask method [Security]","AzScope object","DeleteTask method [Security]","IAzScope interface","IAzScope interface [Security]","DeleteTask method","IAzScope.DeleteTask","IAzScope::DeleteTask","azroles/IAzScope::DeleteTask","security.iazscope_deletetask"]
old-location: security\iazscope_deletetask.htm
tech.root: security
ms.assetid: de72b944-2796-4445-9fdd-4d56526dc903
ms.date: 12/05/2018
ms.keywords: AzScope object [Security],DeleteTask method, DeleteTask, DeleteTask method [Security], DeleteTask method [Security],AzScope object, DeleteTask method [Security],IAzScope interface, IAzScope interface [Security],DeleteTask method, IAzScope.DeleteTask, IAzScope::DeleteTask, azroles/IAzScope::DeleteTask, security.iazscope_deletetask
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
 - IAzScope::DeleteTask
 - azroles/IAzScope::DeleteTask
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
 - IAzScope.DeleteTask
 - AzScope.DeleteTask
---

# IAzScope::DeleteTask


## -description

The <b>DeleteTask</b> method removes the <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object with the specified name from the <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object.

## -parameters

### -param bstrTaskName [in]

Name of the <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object to delete.

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

If there are any <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> references to an <b>IAzTask</b> object that has been deleted from the cache, the <b>IAzTask</b> object can no longer be used. In C++, you must release references to deleted <b>IAzTask</b> objects by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.