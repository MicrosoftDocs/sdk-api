---
UID: NF:azroles.IAzApplication.DeleteApplicationGroup
title: IAzApplication::DeleteApplicationGroup (azroles.h)
description: Removes the IAzApplicationGroup object with the specified name from the IAzApplication object.helpviewer_keywords: ["AzApplication object [Security]","DeleteApplicationGroup method","DeleteApplicationGroup","DeleteApplicationGroup method [Security]","DeleteApplicationGroup method [Security]","AzApplication object","DeleteApplicationGroup method [Security]","IAzApplication interface","IAzApplication interface [Security]","DeleteApplicationGroup method","IAzApplication.DeleteApplicationGroup","IAzApplication::DeleteApplicationGroup","azroles/IAzApplication::DeleteApplicationGroup","security.iazapplication_deleteapplicationgroup"]
old-location: security\iazapplication_deleteapplicationgroup.htm
tech.root: SecAuthZ
ms.assetid: e2ec7ba1-5998-45bf-aacf-e519bb944d5e
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],DeleteApplicationGroup method, DeleteApplicationGroup, DeleteApplicationGroup method [Security], DeleteApplicationGroup method [Security],AzApplication object, DeleteApplicationGroup method [Security],IAzApplication interface, IAzApplication interface [Security],DeleteApplicationGroup method, IAzApplication.DeleteApplicationGroup, IAzApplication::DeleteApplicationGroup, azroles/IAzApplication::DeleteApplicationGroup, security.iazapplication_deleteapplicationgroup
f1_keywords:
- azroles/IAzApplication.DeleteApplicationGroup
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Azroles.dll
api_name:
- IAzApplication.DeleteApplicationGroup
- AzApplication.DeleteApplicationGroup
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzApplication::DeleteApplicationGroup


## -description


The <b>DeleteApplicationGroup</b> method removes the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object with the specified name from the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object.


## -parameters




### -param bstrGroupName [in]

Name of the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object to delete.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



If there are any <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> references to an <b>IAzApplicationGroup</b> object that has been deleted from the cache, the <b>IAzApplicationGroup</b> object can no longer be used. In C++, you must release references to deleted <b>IAzApplicationGroup</b> objects by calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.



