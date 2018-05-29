---
UID: NF:scesvc.ISceSvcAttachmentData.Initialize
title: ISceSvcAttachmentData::Initialize
author: windows-sdk-content
description: The Initialize method informs the Security Configuration snap-in that the snap-in extension is loaded, and it establishes a context for communications.
old-location: security\iscesvcattachmentdata_initialize.htm
old-project: SecMgmt
ms.assetid: 2c5d087d-774b-4cfb-a458-9a5b1c6106c7
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ISceSvcAttachmentData interface [Security],Initialize method, ISceSvcAttachmentData.Initialize, ISceSvcAttachmentData::Initialize, Initialize, Initialize method [Security], Initialize method [Security],ISceSvcAttachmentData interface, _config_iscesvcattachmentdata_initialize, scesvc/ISceSvcAttachmentData::Initialize, security.iscesvcattachmentdata_initialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: scesvc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: SCESVC_INFO_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wsecedit.dll
api_name:
-	ISceSvcAttachmentData.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsecedit.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

