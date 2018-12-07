---
UID: NF:azroles.IAzAuthorizationStore.OpenApplication
title: IAzAuthorizationStore::OpenApplication
author: windows-sdk-content
description: Opens the IAzApplication object with the specified name.
old-location: security\azauthorizationstore_openapplication.htm
tech.root: secauthz
ms.assetid: 63215a9a-b739-4ba9-a760-a9968be9e017
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AzAuthorizationStore object [Security],OpenApplication method, IAzAuthorizationStore interface [Security],OpenApplication method, IAzAuthorizationStore.OpenApplication, IAzAuthorizationStore::OpenApplication, OpenApplication, OpenApplication method [Security], OpenApplication method [Security],AzAuthorizationStore object, OpenApplication method [Security],IAzAuthorizationStore interface, azroles/IAzAuthorizationStore::OpenApplication, security.azauthorizationstore_openapplication
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
 - AzAuthorizationStore.OpenApplication
 - IAzAuthorizationStore.OpenApplication
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzAuthorizationStore::OpenApplication


## -description


The <b>OpenApplication</b> method opens the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object with the specified name.


## -parameters




### -param bstrApplicationName [in]

Name of the <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object to open.


### -param varReserved [in, optional]

Reserved for future use.


### -param ppApplication [out]

A pointer to a pointer to the opened <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object.


## -returns



 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.



