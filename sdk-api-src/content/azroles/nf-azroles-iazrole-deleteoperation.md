---
UID: NF:azroles.IAzRole.DeleteOperation
title: IAzRole::DeleteOperation (azroles.h)
author: windows-sdk-content
description: Removes the IAzOperation object with the specified name from the role.
old-location: security\iazrole_deleteoperation.htm
tech.root: SecAuthZ
ms.assetid: d3486a12-7059-47b8-9f06-a025d5756b70
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AzRole object [Security],DeleteOperation method, DeleteOperation, DeleteOperation method [Security], DeleteOperation method [Security],AzRole object, DeleteOperation method [Security],IAzRole interface, IAzRole interface [Security],DeleteOperation method, IAzRole.DeleteOperation, IAzRole::DeleteOperation, azroles/IAzRole::DeleteOperation, security.iazrole_deleteoperation
ms.topic: method
f1_keywords: ["azroles/IAzRole.DeleteOperation"]
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
 - IAzRole.DeleteOperation
 - AzRole.DeleteOperation
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzRole::DeleteOperation


## -description


The <b>DeleteOperation</b> method removes the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object with the specified name from the role.


## -parameters




### -param bstrProp [in]

Name of the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object to remove from the role.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



If there are any <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> references to an <b>IAzOperation</b> object that has been deleted from the cache, the <b>IAzOperation</b> object can no longer be used. In C++, you must release references to deleted <b>IAzOperation</b> objects by calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.



