---
UID: NF:azroles.IAzAuthorizationStore.DeleteApplicationGroup
title: IAzAuthorizationStore::DeleteApplicationGroup
author: windows-sdk-content
description: Removes the IAzApplicationGroup object with the specified name from the AzAuthorizationStore object.
old-location: security\azauthorizationstore_deleteapplicationgroup.htm
old-project: SecAuthZ
ms.assetid: f2b89378-9b4e-411f-b856-51053b649996
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AzAuthorizationStore object [Security],DeleteApplicationGroup method, DeleteApplicationGroup, DeleteApplicationGroup method [Security], DeleteApplicationGroup method [Security],AzAuthorizationStore object, DeleteApplicationGroup method [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],DeleteApplicationGroup method, IAzAuthorizationStore.DeleteApplicationGroup, IAzAuthorizationStore::DeleteApplicationGroup, azroles/IAzAuthorizationStore::DeleteApplicationGroup, security.azauthorizationstore_deleteapplicationgroup
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
 - AzAuthorizationStore.DeleteApplicationGroup
 - IAzAuthorizationStore.DeleteApplicationGroup
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzAuthorizationStore::DeleteApplicationGroup


## -description


The <b>DeleteApplicationGroup</b> method removes the <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object with the specified name from the <a href="https://msdn.microsoft.com/f848cca6-3838-46bc-b1f4-d6eab5096046">AzAuthorizationStore</a> object.


## -parameters




### -param bstrGroupName [in]

Name of the <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object to delete.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



If there are any <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> references to an <b>IAzApplicationGroup</b> object that has been deleted from the cache, the <b>IAzApplicationGroup</b> object can no longer be used. In C++, you must release references to deleted <b>IAzApplicationGroup</b> objects by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method. In  Visual Basic, references to deleted objects are automatically released.



