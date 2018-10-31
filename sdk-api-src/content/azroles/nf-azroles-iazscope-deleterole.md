---
UID: NF:azroles.IAzScope.DeleteRole
title: IAzScope::DeleteRole
author: windows-sdk-content
description: Removes the IAzRole object with the specified name from the IAzScope object.
old-location: security\iazscope_deleterole.htm
tech.root: secauthz
ms.assetid: 9155c4f8-ad17-402e-80a1-3dcee044d2c4
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: AzScope object [Security],DeleteRole method, DeleteRole, DeleteRole method [Security], DeleteRole method [Security],AzScope object, DeleteRole method [Security],IAzScope interface, IAzScope interface [Security],DeleteRole method, IAzScope.DeleteRole, IAzScope::DeleteRole, azroles/IAzScope::DeleteRole, security.iazscope_deleterole
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
 - IAzScope.DeleteRole
 - AzScope.DeleteRole
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzScope::DeleteRole


## -description


The <b>DeleteRole</b> method removes the <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> object with the specified name from the <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object.


## -parameters




### -param bstrRoleName [in]

Name of the <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> object to delete.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



If there are any <a href="https://msdn.microsoft.com/2934d783-b379-486c-80e7-e7650b89dc1a">IAzRole</a> references to an <b>IAzRole</b> object that has been deleted from the cache, the <b>IAzRole</b> object can no longer be used. In C++, you must release references to deleted <b>IAzRole</b> objects by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.



