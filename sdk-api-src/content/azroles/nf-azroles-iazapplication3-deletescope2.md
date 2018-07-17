---
UID: NF:azroles.IAzApplication3.DeleteScope2
title: IAzApplication3::DeleteScope2
author: windows-sdk-content
description: Removes the specified IAzScope2 object from the IAzApplication3 object.
old-location: security\iazapplication3_deletescope2.htm
old-project: secauthz
ms.assetid: f42f9288-896b-4034-a16c-3d555acea453
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: DeleteScope2, DeleteScope2 method [Security], DeleteScope2 method [Security],IAzApplication3 interface, IAzApplication3 interface [Security],DeleteScope2 method, IAzApplication3.DeleteScope2, IAzApplication3::DeleteScope2, azroles/IAzApplication3::DeleteScope2, security.iazapplication3_deletescope2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IAzApplication3.DeleteScope2
product: Windows
targetos: Windows
req.lib: 
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication3::DeleteScope2


## -description


The <b>DeleteScope2</b> method removes the specified <a href="https://msdn.microsoft.com/536c563e-7a6b-480d-9e83-1d7cc90a795d">IAzScope2</a> object from the <a href="https://msdn.microsoft.com/9d0b2c3b-b8b6-4fae-9308-9dd29da0724f">IAzApplication3</a> object.


## -parameters




### -param bstrScopeName [in]

A string that contains the name of the <a href="https://msdn.microsoft.com/536c563e-7a6b-480d-9e83-1d7cc90a795d">IAzScope2</a> object to remove.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



If any references to an <a href="https://msdn.microsoft.com/536c563e-7a6b-480d-9e83-1d7cc90a795d">IAzScope2</a> object have been deleted from the cache, you can no longer user that object. In C++, you must release references to deleted <b>IAzScope2</b> objects by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.



