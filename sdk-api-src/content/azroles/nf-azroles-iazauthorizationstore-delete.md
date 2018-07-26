---
UID: NF:azroles.IAzAuthorizationStore.Delete
title: IAzAuthorizationStore::Delete
author: windows-sdk-content
description: Deletes the policy store currently in use by the AzAuthorizationStore object.
old-location: security\azauthorizationstore_delete.htm
old-project: secauthz
ms.assetid: 8493af39-c5db-4aeb-839f-bc07e2616443
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: AzAuthorizationStore object [Security],Delete method, Delete, Delete method [Security], Delete method [Security],AzAuthorizationStore object, Delete method [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],Delete method, IAzAuthorizationStore.Delete, IAzAuthorizationStore::Delete, azroles/IAzAuthorizationStore::Delete, security.azauthorizationstore_delete
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
 - AzAuthorizationStore.Delete
 - IAzAuthorizationStore.Delete
product: Windows
targetos: Windows
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
---

# IAzAuthorizationStore::Delete


## -description


The <b>Delete</b> method deletes the policy store currently in use by the <a href="https://msdn.microsoft.com/f848cca6-3838-46bc-b1f4-d6eab5096046">AzAuthorizationStore</a> object.


## -parameters




### -param varReserved [in, optional]

Reserved for future use.


## -remarks



When the <b>Delete</b> method is called, the <a href="https://msdn.microsoft.com/f848cca6-3838-46bc-b1f4-d6eab5096046">AzAuthorizationStore</a> object returns to an uninitialized state. The <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method can then be called to reinitialize the object. 

<div class="alert"><b>Important</b>  All objects opened by clients on the policy store  (for example,  <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> objects created using <a href="https://msdn.microsoft.com/ca6feb69-15cd-454a-a2b8-c75c4c6b38cd">CreateApplication</a>) must be released before you call the <b>Delete</b> method. If the <b>Delete</b> method is called on an <a href="https://msdn.microsoft.com/f848cca6-3838-46bc-b1f4-d6eab5096046">AzAuthorizationStore</a> object whose current policy store contains child objects, HRESULT_FROM_WIN32(ERROR_SERVER_HAS_OPEN_HANDLES) is returned.</div>
<div> </div>


