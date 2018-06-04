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

# ISceSvcAttachmentData::CloseHandle


## -description


The <b>CloseHandle</b> method closes a handle opened during a previous call to 
<a href="https://msdn.microsoft.com/2c5d087d-774b-4cfb-a458-9a5b1c6106c7">ISceSvcAttachmentData::Initialize</a>.


## -parameters




### -param scesvcHandle






#### - sceHandle [in]

The 
<a href="https://msdn.microsoft.com/478d7d4b-7983-4247-b8be-2e2cd3327533">SCESVC_HANDLE</a> to close.


## -returns



The return value is an <b>HRESULT</b>. A value of <b>S_OK</b> indicates the method was successful.




## -remarks



You should call this method when your attachment snap-in extension no longer requires the handle returned by 
<a href="https://msdn.microsoft.com/2c5d087d-774b-4cfb-a458-9a5b1c6106c7">ISceSvcAttachmentData::Initialize</a>.




## -see-also




<a href="https://msdn.microsoft.com/385acdb9-5642-47c1-b2ac-be388edaac12">ISceSvcAttachmentData</a>



<a href="https://msdn.microsoft.com/2c5d087d-774b-4cfb-a458-9a5b1c6106c7">ISceSvcAttachmentData::Initialize</a>
 

 

