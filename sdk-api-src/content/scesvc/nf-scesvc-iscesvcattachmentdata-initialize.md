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

# ISceSvcAttachmentData::Initialize


## -description


The <b>Initialize</b> method informs the Security Configuration snap-in that the snap-in extension is loaded, and it establishes a context for communications.


## -parameters




### -param lpServiceName




### -param lpTemplateName




### -param lpSceSvcPersistInfo [in]

Pointer to the 
<a href="https://msdn.microsoft.com/3cd4bde2-55f6-4ab1-b175-7689b0cc529b">ISceSvcAttachmentPersistInfo</a> interface of the attachment snap-in extension.


### -param pscesvcHandle






#### - ServiceName [in]

String that specifies the name of the security service to retrieve information about.


#### - TemplateName [in]

String that specifies the name of the template.


#### - sceHandle [out]

Pointer that receives an 
<a href="https://msdn.microsoft.com/478d7d4b-7983-4247-b8be-2e2cd3327533">SCESVC_HANDLE</a> that represents the communication context between the Security Configuration snap-in and the snap-in extension. This handle is passed in as a parameter to the other <a href="https://msdn.microsoft.com/385acdb9-5642-47c1-b2ac-be388edaac12">ISceSvcAttachmentData</a> methods. When the attachment snap-in extension no longer needs this handle, free it by calling 
<a href="https://msdn.microsoft.com/e50f5acf-06ef-49bb-bcf1-1fadeb4b808a">ISceSvcAttachmentData::CloseHandle</a>.


## -returns



The return value is an HRESULT. A value of S_OK indicates the method was successful.




## -see-also




<a href="https://msdn.microsoft.com/385acdb9-5642-47c1-b2ac-be388edaac12">ISceSvcAttachmentData</a>



<a href="https://msdn.microsoft.com/e50f5acf-06ef-49bb-bcf1-1fadeb4b808a">ISceSvcAttachmentData::CloseHandle</a>



<a href="https://msdn.microsoft.com/3cd4bde2-55f6-4ab1-b175-7689b0cc529b">ISceSvcAttachmentPersistInfo</a>



<a href="https://msdn.microsoft.com/478d7d4b-7983-4247-b8be-2e2cd3327533">SCESVC_HANDLE</a>
 

 

