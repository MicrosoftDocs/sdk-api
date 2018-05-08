---
UID: NF:scesvc.ISceSvcAttachmentPersistInfo.IsDirty
title: ISceSvcAttachmentPersistInfo::IsDirty
author: windows-driver-content
description: The IsDirty method returns a value indicating whether data in the attachment snap-in has been modified since it was last saved.
old-location: security\iscesvcattachmentpersistinfo_isdirty.htm
old-project: SecMgmt
ms.assetid: b430e598-e16c-47fc-8f19-fbcfc6b71337
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ISceSvcAttachmentPersistInfo interface [Security],IsDirty method, ISceSvcAttachmentPersistInfo.IsDirty, ISceSvcAttachmentPersistInfo::IsDirty, IsDirty, IsDirty method [Security], IsDirty method [Security],ISceSvcAttachmentPersistInfo interface, _config_iscesvcattachmentpersistinfo_isdirty, scesvc/ISceSvcAttachmentPersistInfo::IsDirty, security.iscesvcattachmentpersistinfo_isdirty
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	ISceSvcAttachmentPersistInfo.IsDirty
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsecedit.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ISceSvcAttachmentPersistInfo::IsDirty


## -description


The <b>IsDirty</b> method returns a value indicating whether data in the attachment snap-in has been modified since it was last saved.


## -parameters




### -param lpTemplateName [in]

Pointer to a null-terminated string that contains a security template name. Multiple security templates can be modified so that each service extension can be expanded under multiple templates.


## -returns



The return value is an HRESULT. A value of S_OK indicates the method was successful.




## -see-also




<a href="https://msdn.microsoft.com/3cd4bde2-55f6-4ab1-b175-7689b0cc529b">ISceSvcAttachmentPersistInfo</a>



<a href="https://msdn.microsoft.com/bdec64b8-2a92-4165-95ff-0de981f2d878">ISceSvcAttachmentPersistInfo::Save</a>
 

 

