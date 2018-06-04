---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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


