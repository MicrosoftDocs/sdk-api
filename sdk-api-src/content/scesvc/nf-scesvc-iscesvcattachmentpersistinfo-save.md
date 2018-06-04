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

# ISceSvcAttachmentPersistInfo::Save


## -description


The <b>Save</b> method causes the snap-in extension to return information about the data that needs to be saved. The caller is responsible for saving the data.


## -parameters




### -param lpTemplateName [in]

Pointer to a null-terminated string that contains the security template name to save data to.


### -param scesvcHandle




### -param ppvData [out]

Pointer that receives a buffer that contains the data to be saved.


### -param pbOverwriteAll






#### - pbOverWriteAll [out]

Pointer to a <b>BOOL</b> that receives a value indicating whether preexisting data should be overwritten.


#### - sceHandle [in]

Pointer that receives the 
<a href="https://msdn.microsoft.com/478d7d4b-7983-4247-b8be-2e2cd3327533">SCESVC_HANDLE</a> the attachment snap-in extension is using to communicate with the Security Configuration snap-ins.


## -returns



The return value is an HRESULT. A value of S_OK indicates the method was successful.




## -remarks



The caller should free the buffer set in <i>ppvData</i> by calling 
<a href="https://msdn.microsoft.com/b41f01a4-dc38-4954-a3c5-19fa72910d6f">ISceSvcAttachmentPersistInfo::FreeBuffer</a>.




## -see-also




<a href="https://msdn.microsoft.com/3cd4bde2-55f6-4ab1-b175-7689b0cc529b">ISceSvcAttachmentPersistInfo</a>



<a href="https://msdn.microsoft.com/b41f01a4-dc38-4954-a3c5-19fa72910d6f">ISceSvcAttachmentPersistInfo::FreeBuffer</a>



<a href="https://msdn.microsoft.com/b430e598-e16c-47fc-8f19-fbcfc6b71337">ISceSvcAttachmentPersistInfo::IsDirty</a>



<a href="https://msdn.microsoft.com/478d7d4b-7983-4247-b8be-2e2cd3327533">SCESVC_HANDLE</a>
 

 

