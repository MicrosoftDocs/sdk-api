---
UID: NF:azroles.IAzApplication.DeleteRole
title: IAzApplication::DeleteRole
author: windows-sdk-content
description: Removes the IAzRole object with the specified name from the IAzApplication object.
old-location: security\iazapplication_deleterole.htm
tech.root: SecAuthZ
ms.assetid: c97c271a-f08c-481e-9787-61518d8cbb73
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: AzApplication object [Security],DeleteRole method, DeleteRole, DeleteRole method [Security], DeleteRole method [Security],AzApplication object, DeleteRole method [Security],IAzApplication interface, IAzApplication interface [Security],DeleteRole method, IAzApplication.DeleteRole, IAzApplication::DeleteRole, azroles/IAzApplication::DeleteRole, security.iazapplication_deleterole
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
 - IAzApplication.DeleteRole
 - AzApplication.DeleteRole
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzApplication::DeleteRole


## -description


The <b>DeleteRole</b> method removes the <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> object with the specified name from the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object.


## -parameters




### -param bstrRoleName [in]

Name of the <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> object to delete.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



If there are any <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> references to an <b>IAzRole</b> object that has been deleted from the cache, the <b>IAzRole</b> object can no longer be used. In C++, you must release references to deleted <b>IAzRole</b> objects by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.



