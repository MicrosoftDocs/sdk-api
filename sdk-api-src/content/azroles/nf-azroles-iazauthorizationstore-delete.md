---
UID: NF:azroles.IAzAuthorizationStore.Delete
title: IAzAuthorizationStore::Delete
author: windows-sdk-content
description: Deletes the policy store currently in use by the AzAuthorizationStore object.
old-location: security\azauthorizationstore_delete.htm
tech.root: SecAuthZ
ms.assetid: 8493af39-c5db-4aeb-839f-bc07e2616443
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AzAuthorizationStore object [Security],Delete method, Delete, Delete method [Security], Delete method [Security],AzAuthorizationStore object, Delete method [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],Delete method, IAzAuthorizationStore.Delete, IAzAuthorizationStore::Delete, azroles/IAzAuthorizationStore::Delete, security.azauthorizationstore_delete
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
 - AzAuthorizationStore.Delete
 - IAzAuthorizationStore.Delete
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
---

# IAzAuthorizationStore::Delete


## -description


The <b>Delete</b> method deletes the policy store currently in use by the <a href="https://msdn.microsoft.com/en-us/library/Aa376327(v=VS.85).aspx">AzAuthorizationStore</a> object.


## -parameters




### -param varReserved [in, optional]

Reserved for future use.


## -remarks



When the <b>Delete</b> method is called, the <a href="https://msdn.microsoft.com/en-us/library/Aa376327(v=VS.85).aspx">AzAuthorizationStore</a> object returns to an uninitialized state. The <a href="https://msdn.microsoft.com/en-us/library/Aa376359(v=VS.85).aspx">Initialize</a> method can then be called to reinitialize the object. 

<div class="alert"><b>Important</b>  All objects opened by clients on the policy store  (for example,  <a href="https://msdn.microsoft.com/en-us/library/Aa446684(v=VS.85).aspx">IAzApplication</a> objects created using <a href="https://msdn.microsoft.com/en-us/library/Aa376341(v=VS.85).aspx">CreateApplication</a>) must be released before you call the <b>Delete</b> method. If the <b>Delete</b> method is called on an <a href="https://msdn.microsoft.com/en-us/library/Aa376327(v=VS.85).aspx">AzAuthorizationStore</a> object whose current policy store contains child objects, HRESULT_FROM_WIN32(ERROR_SERVER_HAS_OPEN_HANDLES) is returned.</div>
<div> </div>


