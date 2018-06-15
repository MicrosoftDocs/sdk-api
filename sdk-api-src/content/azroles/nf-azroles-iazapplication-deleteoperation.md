---
UID: NF:azroles.IAzApplication.DeleteOperation
title: IAzApplication::DeleteOperation
author: windows-sdk-content
description: Removes the IAzOperation object with the specified name from the IAzApplication object.
old-location: security\iazapplication_deleteoperation.htm
old-project: SecAuthZ
ms.assetid: 2541e01d-20a4-424f-b8e0-5d6dedfbd7fe
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AzApplication object [Security],DeleteOperation method, DeleteOperation, DeleteOperation method [Security], DeleteOperation method [Security],AzApplication object, DeleteOperation method [Security],IAzApplication interface, IAzApplication interface [Security],DeleteOperation method, IAzApplication.DeleteOperation, IAzApplication::DeleteOperation, azroles/IAzApplication::DeleteOperation, security.iazapplication_deleteoperation
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
 - IAzApplication.DeleteOperation
 - AzApplication.DeleteOperation
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzApplication::DeleteOperation


## -description


The <b>DeleteOperation</b> method removes the <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> object with the specified name from the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object.


## -parameters




### -param bstrOperationName [in]

Name of the <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> object to delete.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



If there are any <a href="https://msdn.microsoft.com/054fa4aa-70be-4618-a635-3941c830ea4e">IAzOperation</a> references to an <b>IAzOperation</b> object that has been deleted from the cache, the <b>IAzOperation</b> object can no longer be used. In C++, you must release references to deleted <b>IAzOperation</b> objects by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.



