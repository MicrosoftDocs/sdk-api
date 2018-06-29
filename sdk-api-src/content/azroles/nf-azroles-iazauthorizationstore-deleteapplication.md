---
UID: NF:azroles.IAzAuthorizationStore.DeleteApplication
title: IAzAuthorizationStore::DeleteApplication
author: windows-sdk-content
description: Removes the IAzApplication object with the specified name from the AzAuthorizationStore object.
old-location: security\azauthorizationstore_deleteapplication.htm
old-project: SecAuthZ
ms.assetid: 512907fc-8657-4f2a-8b4a-af3027c6bbcd
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AzAuthorizationStore object [Security],DeleteApplication method, DeleteApplication, DeleteApplication method [Security], DeleteApplication method [Security],AzAuthorizationStore object, DeleteApplication method [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],DeleteApplication method, IAzAuthorizationStore.DeleteApplication, IAzAuthorizationStore::DeleteApplication, azroles/IAzAuthorizationStore::DeleteApplication, security.azauthorizationstore_deleteapplication
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
 - AzAuthorizationStore.DeleteApplication
 - IAzAuthorizationStore.DeleteApplication
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzAuthorizationStore::DeleteApplication


## -description


The <b>DeleteApplication</b> method removes the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object with the specified name from the <a href="https://msdn.microsoft.com/f848cca6-3838-46bc-b1f4-d6eab5096046">AzAuthorizationStore</a> object.


## -parameters




### -param bstrApplicationName [in]

Name of the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object to delete.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



If the deleted <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object has child objects, those objects are deleted, as well. If there are any <b>IAzApplication</b> references to an <b>IAzApplication</b> object that has been deleted from the cache, the <b>IAzApplication</b> object can no longer be used. In C++, you must release references to deleted <b>IAzApplication</b> objects by calling the <a href="https://msdn.microsoft.com/library/Dd757102(v=VS.85).aspx">IUnknown::Release</a> method. In  Visual Basic, references to deleted objects are automatically released.



