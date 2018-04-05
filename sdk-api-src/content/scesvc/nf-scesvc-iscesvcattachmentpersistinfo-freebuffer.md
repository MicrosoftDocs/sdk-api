---
UID: NF:scesvc.ISceSvcAttachmentPersistInfo.FreeBuffer
title: ISceSvcAttachmentPersistInfo::FreeBuffer method
author: windows-driver-content
description: The FreeBuffer method frees memory allocated by the attachment snap-in extension.
old-location: security\iscesvcattachmentpersistinfo_freebuffer.htm
old-project: SecMgmt
ms.assetid: b41f01a4-dc38-4954-a3c5-19fa72910d6f
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: FreeBuffer method [Security], FreeBuffer method [Security], ISceSvcAttachmentPersistInfo interface, FreeBuffer,ISceSvcAttachmentPersistInfo.FreeBuffer, ISceSvcAttachmentPersistInfo, ISceSvcAttachmentPersistInfo interface [Security], FreeBuffer method, ISceSvcAttachmentPersistInfo::FreeBuffer, _config_iscesvcattachmentpersistinfo_freebuffer, scesvc/ISceSvcAttachmentPersistInfo::FreeBuffer, security.iscesvcattachmentpersistinfo_freebuffer
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
-	ISceSvcAttachmentPersistInfo.FreeBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsecedit.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ISceSvcAttachmentPersistInfo::FreeBuffer method


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
 

 

