---
UID: NF:azroles.IAzAuthorizationStore.OpenApplicationGroup
title: IAzAuthorizationStore::OpenApplicationGroup
author: windows-sdk-content
description: Opens an IAzApplicationGroup object by specifying its name.
old-location: security\azauthorizationstore_openapplicationgroup.htm
tech.root: SecAuthZ
ms.assetid: 30860261-c792-4610-b217-7c4d58554778
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AzAuthorizationStore object [Security],OpenApplicationGroup method, IAzAuthorizationStore interface [Security],OpenApplicationGroup method, IAzAuthorizationStore.OpenApplicationGroup, IAzAuthorizationStore::OpenApplicationGroup, OpenApplicationGroup, OpenApplicationGroup method [Security], OpenApplicationGroup method [Security],AzAuthorizationStore object, OpenApplicationGroup method [Security],IAzAuthorizationStore interface, azroles/IAzAuthorizationStore::OpenApplicationGroup, security.azauthorizationstore_openapplicationgroup
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
 - AzAuthorizationStore.OpenApplicationGroup
 - IAzAuthorizationStore.OpenApplicationGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
- apiref
: 
- COM
: 
- azroles.h
: 
- IAzAuthorizationStore.OpenApplicationGroup
: 
---

# IAzAuthorizationStore::OpenApplicationGroup


## -description


The <b>OpenApplicationGroup</b> method opens an <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object with the specified name.


## -parameters




### -param bstrGroupName [in]

Name of the <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object to open.


### -param varReserved [in, optional]

Reserved for future use.


### -param ppGroup [out]

A pointer to a pointer to the opened <a href="https://msdn.microsoft.com/6a15acde-e582-4c49-b7e4-82d4e54012b1">IAzApplicationGroup</a> object.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.



