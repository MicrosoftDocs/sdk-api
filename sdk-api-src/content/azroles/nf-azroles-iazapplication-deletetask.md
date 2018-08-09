---
UID: NF:azroles.IAzApplication.DeleteTask
title: IAzApplication::DeleteTask
author: windows-sdk-content
description: Removes the IAzTask object with the specified name from the IAzApplication object.
old-location: security\iazapplication_deletetask.htm
old-project: secauthz
ms.assetid: b97015d7-00c3-445c-a445-07c52ef6ff29
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AzApplication object [Security],DeleteTask method, DeleteTask, DeleteTask method [Security], DeleteTask method [Security],AzApplication object, DeleteTask method [Security],IAzApplication interface, IAzApplication interface [Security],DeleteTask method, IAzApplication.DeleteTask, IAzApplication::DeleteTask, azroles/IAzApplication::DeleteTask, security.iazapplication_deletetask
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
 - IAzApplication.DeleteTask
 - AzApplication.DeleteTask
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication::DeleteTask


## -description


The <b>DeleteTask</b> method removes the <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object with the specified name from the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object.


## -parameters




### -param bstrTaskName [in]

Name of the <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> object to delete.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



If there are any <a href="https://msdn.microsoft.com/90eb19c9-1490-43f4-ab4b-393e825aeb2f">IAzTask</a> references to an <b>IAzTask</b> object that has been deleted from the cache, the <b>IAzTask</b> object can no longer be used. In C++, you must release references to deleted <b>IAzTask</b> objects by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.



