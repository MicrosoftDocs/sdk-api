---
UID: NF:azroles.IAzApplication.DeleteApplicationGroup
title: IAzApplication::DeleteApplicationGroup
author: windows-sdk-content
description: Removes the IAzApplicationGroup object with the specified name from the IAzApplication object.
old-location: security\iazapplication_deleteapplicationgroup.htm
old-project: secauthz
ms.assetid: e2ec7ba1-5998-45bf-aacf-e519bb944d5e
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: AzApplication object [Security],DeleteApplicationGroup method, DeleteApplicationGroup, DeleteApplicationGroup method [Security], DeleteApplicationGroup method [Security],AzApplication object, DeleteApplicationGroup method [Security],IAzApplication interface, IAzApplication interface [Security],DeleteApplicationGroup method, IAzApplication.DeleteApplicationGroup, IAzApplication::DeleteApplicationGroup, azroles/IAzApplication::DeleteApplicationGroup, security.iazapplication_deleteapplicationgroup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
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
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication::DeleteApplicationGroup


## -description


The <b>DeleteApplicationGroup</b> method removes the <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object with the specified name from the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object.


## -parameters




### -param bstrGroupName [in]

Name of the <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object to delete.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



If there are any <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> references to an <b>IAzApplicationGroup</b> object that has been deleted from the cache, the <b>IAzApplicationGroup</b> object can no longer be used. In C++, you must release references to deleted <b>IAzApplicationGroup</b> objects by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.



