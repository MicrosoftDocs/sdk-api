---
UID: NF:azroles.IAzScope.DeleteApplicationGroup
title: IAzScope::DeleteApplicationGroup
author: windows-sdk-content
description: Removes the IAzApplicationGroup object with the specified name from the IAzScope object.
old-location: security\iazscope_deleteapplicationgroup.htm
tech.root: SecAuthZ
ms.assetid: 9571bff3-dfe5-48fa-be51-38d61da40414
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AzScope object [Security],DeleteApplicationGroup method, DeleteApplicationGroup, DeleteApplicationGroup method [Security], DeleteApplicationGroup method [Security],AzScope object, DeleteApplicationGroup method [Security],IAzScope interface, IAzScope interface [Security],DeleteApplicationGroup method, IAzScope.DeleteApplicationGroup, IAzScope::DeleteApplicationGroup, azroles/IAzScope::DeleteApplicationGroup, security.iazscope_deleteapplicationgroup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IAzScope.DeleteApplicationGroup
 - AzScope.DeleteApplicationGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
- apiref
: 
- COM
: 
- azroles.h
: 
- IAzScope.DeleteApplicationGroup
: 
---

# IAzScope::DeleteApplicationGroup


## -description


The <b>DeleteApplicationGroup</b> method removes the <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object with the specified name from the <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object.


## -parameters




### -param bstrGroupName [in]

Name of the <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object to delete.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



If there are any <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> references to an <b>IAzApplicationGroup</b> object that has been deleted from the cache, the <b>IAzApplicationGroup</b> object can no longer be used. In C++, you must release references to deleted <b>IAzApplicationGroup</b> objects by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.



