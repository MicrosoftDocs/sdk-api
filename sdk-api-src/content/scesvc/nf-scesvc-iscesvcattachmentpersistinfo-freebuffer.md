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

# ISceSvcAttachmentPersistInfo::FreeBuffer


## -description


The <b>FreeBuffer</b> method frees memory allocated by the attachment snap-in extension.


## -parameters




### -param pvData [in]

Pointer to the buffer to free.


## -returns



The return value is an HRESULT. A value of S_OK indicates the method was successful.




## -remarks



You should call this method to free the data buffer returned by 
<a href="https://msdn.microsoft.com/bdec64b8-2a92-4165-95ff-0de981f2d878">ISceSvcAttachmentPersistInfo::Save</a>.




## -see-also




<a href="https://msdn.microsoft.com/3cd4bde2-55f6-4ab1-b175-7689b0cc529b">ISceSvcAttachmentPersistInfo</a>



<a href="https://msdn.microsoft.com/bdec64b8-2a92-4165-95ff-0de981f2d878">ISceSvcAttachmentPersistInfo::Save</a>
 

 

