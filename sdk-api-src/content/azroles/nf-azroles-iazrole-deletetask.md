---
UID: NF:azroles.IAzRole.DeleteTask
title: IAzRole::DeleteTask
author: windows-sdk-content
description: Removes the IAzTask object with the specified name from the role.
old-location: security\iazrole_deletetask.htm
old-project: secauthz
ms.assetid: 62623d45-33a6-4e3f-b0a8-d3e3e7c9e33e
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: AzRole object [Security],DeleteTask method, DeleteTask, DeleteTask method [Security], DeleteTask method [Security],AzRole object, DeleteTask method [Security],IAzRole interface, IAzRole interface [Security],DeleteTask method, IAzRole.DeleteTask, IAzRole::DeleteTask, azroles/IAzRole::DeleteTask, security.iazrole_deletetask
ms.prod: windows
ms.technology: windows-sdk
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
 - IAzRole.DeleteTask
 - AzRole.DeleteTask
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzRole::DeleteTask


## -description


The <b>DeleteTask</b> method removes the <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object with the specified name from the role.


## -parameters




### -param bstrProp [in]

Name of the <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object to remove from the role.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



If there are any <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> references to an <b>IAzTask</b> object that has been deleted from the cache, the <b>IAzTask</b> object can no longer be used. In C++, you must release references to deleted <b>IAzTask</b> objects by calling the <a href="https://msdn.microsoft.com/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.



