---
UID: NF:azroles.IAzAuthorizationStore.DeleteApplicationGroup
title: IAzAuthorizationStore::DeleteApplicationGroup
author: windows-sdk-content
description: Removes the IAzApplicationGroup object with the specified name from the AzAuthorizationStore object.
old-location: security\azauthorizationstore_deleteapplicationgroup.htm
tech.root: SecAuthZ
ms.assetid: f2b89378-9b4e-411f-b856-51053b649996
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: AzAuthorizationStore object [Security],DeleteApplicationGroup method, DeleteApplicationGroup, DeleteApplicationGroup method [Security], DeleteApplicationGroup method [Security],AzAuthorizationStore object, DeleteApplicationGroup method [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],DeleteApplicationGroup method, IAzAuthorizationStore.DeleteApplicationGroup, IAzAuthorizationStore::DeleteApplicationGroup, azroles/IAzAuthorizationStore::DeleteApplicationGroup, security.azauthorizationstore_deleteapplicationgroup
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
 - AzAuthorizationStore.DeleteApplicationGroup
 - IAzAuthorizationStore.DeleteApplicationGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzAuthorizationStore::DeleteApplicationGroup


## -description


The <b>DeleteApplicationGroup</b> method removes the <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroup</a> object with the specified name from the <a href="https://msdn.microsoft.com/en-us/library/Aa376327(v=VS.85).aspx">AzAuthorizationStore</a> object.


## -parameters




### -param bstrGroupName [in]

Name of the <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroup</a> object to delete.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



If there are any <a href="https://msdn.microsoft.com/en-us/library/Aa377253(v=VS.85).aspx">IAzApplicationGroup</a> references to an <b>IAzApplicationGroup</b> object that has been deleted from the cache, the <b>IAzApplicationGroup</b> object can no longer be used. In C++, you must release references to deleted <b>IAzApplicationGroup</b> objects by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method. In  Visual Basic, references to deleted objects are automatically released.



