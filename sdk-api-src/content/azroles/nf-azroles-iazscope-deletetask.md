---
UID: NF:azroles.IAzScope.DeleteTask
title: IAzScope::DeleteTask
author: windows-sdk-content
description: Removes the IAzTask object with the specified name from the IAzScope object.
old-location: security\iazscope_deletetask.htm
old-project: SecAuthZ
ms.assetid: de72b944-2796-4445-9fdd-4d56526dc903
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AzScope object [Security],DeleteTask method, DeleteTask, DeleteTask method [Security], DeleteTask method [Security],AzScope object, DeleteTask method [Security],IAzScope interface, IAzScope interface [Security],DeleteTask method, IAzScope.DeleteTask, IAzScope::DeleteTask, azroles/IAzScope::DeleteTask, security.iazscope_deletetask
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
 - IAzScope.DeleteTask
 - AzScope.DeleteTask
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzScope::DeleteTask


## -description


The <b>DeleteTask</b> method removes the <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object with the specified name from the <a href="https://msdn.microsoft.com/f7abe7cb-8827-46f6-85fe-99282582a3d4">IAzScope</a> object.


## -parameters




### -param bstrTaskName [in]

Name of the <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object to delete.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



If there are any <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> references to an <b>IAzTask</b> object that has been deleted from the cache, the <b>IAzTask</b> object can no longer be used. In C++, you must release references to deleted <b>IAzTask</b> objects by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release.md">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.



