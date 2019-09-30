---
UID: NF:scesvc.ISceSvcAttachmentPersistInfo.FreeBuffer
title: ISceSvcAttachmentPersistInfo::FreeBuffer (scesvc.h)
author: windows-sdk-content
description: The FreeBuffer method frees memory allocated by the attachment snap-in extension.
old-location: security\iscesvcattachmentpersistinfo_freebuffer.htm
tech.root: SecMgmt
ms.assetid: b41f01a4-dc38-4954-a3c5-19fa72910d6f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FreeBuffer, FreeBuffer method [Security], FreeBuffer method [Security],ISceSvcAttachmentPersistInfo interface, ISceSvcAttachmentPersistInfo interface [Security],FreeBuffer method, ISceSvcAttachmentPersistInfo.FreeBuffer, ISceSvcAttachmentPersistInfo::FreeBuffer, _config_iscesvcattachmentpersistinfo_freebuffer, scesvc/ISceSvcAttachmentPersistInfo::FreeBuffer, security.iscesvcattachmentpersistinfo_freebuffer
ms.topic: method
f1_keywords: 
 - "scesvc/ISceSvcAttachmentPersistInfo.FreeBuffer"
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
req.lib: 
req.dll: Wsecedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsecedit.dll
api_name:
 - ISceSvcAttachmentPersistInfo.FreeBuffer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/windows/desktop/api/scesvc/nf-scesvc-iscesvcattachmentpersistinfo-save">ISceSvcAttachmentPersistInfo::Save</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/scesvc/nn-scesvc-iscesvcattachmentpersistinfo">ISceSvcAttachmentPersistInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/scesvc/nf-scesvc-iscesvcattachmentpersistinfo-save">ISceSvcAttachmentPersistInfo::Save</a>
 

 

