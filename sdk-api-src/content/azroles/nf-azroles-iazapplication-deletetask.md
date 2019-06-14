---
UID: NF:azroles.IAzApplication.DeleteTask
title: IAzApplication::DeleteTask (azroles.h)
author: windows-sdk-content
description: Removes the IAzTask object with the specified name from the IAzApplication object.
old-location: security\iazapplication_deletetask.htm
tech.root: SecAuthZ
ms.assetid: b97015d7-00c3-445c-a445-07c52ef6ff29
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],DeleteTask method, DeleteTask, DeleteTask method [Security], DeleteTask method [Security],AzApplication object, DeleteTask method [Security],IAzApplication interface, IAzApplication interface [Security],DeleteTask method, IAzApplication.DeleteTask, IAzApplication::DeleteTask, azroles/IAzApplication::DeleteTask, security.iazapplication_deletetask
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
 - IAzApplication.DeleteTask
 - AzApplication.DeleteTask
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzApplication::DeleteTask


## -description


The <b>DeleteTask</b> method removes the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object with the specified name from the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object.


## -parameters




### -param bstrTaskName [in]

Name of the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object to delete.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



If there are any <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> references to an <b>IAzTask</b> object that has been deleted from the cache, the <b>IAzTask</b> object can no longer be used. In C++, you must release references to deleted <b>IAzTask</b> objects by calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.



